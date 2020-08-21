# Gitlab 
## Gitlab runner

#### Use local system volume mounts to start the Runner container
```sh
$ docker run -d --name gitlab-runner --restart always \
    -v /srv/gitlab-runner/config:/etc/gitlab-runner \
    -v /var/run/docker.sock:/var/run/docker.sock \
    gitlab/gitlab-runner:latest
```
#### Registry a new docker runner
```sh
$ docker run --rm -it -v /srv/gitlab-runner/config:/etc/gitlab-runner gitlab/gitlab-runner register
```

#### Docker insecure registries
```sh
$ touch /etc/docker/daemon.json 
-------------------------------
{
    "insecure-registries" : ["registry.gitlab.kronostoken.com"]
}
```
#### Use Docker socket binding
```
[[runners]]
  url = "https://gitlab.com/"
  token = REGISTRATION_TOKEN
  executor = "docker"
  [runners.docker]
    tls_verify = false
    image = "docker:19.03.12"
    privileged = false
    disable_cache = false
    volumes = ["`/var/run/docker.sock:/var/run/docker.sock`", "/cache"]   # make the CI-container created by gitlab runner can use local docker engine
  [runers.cache]
    Insecure = false
```

# Reference
[Run GitLab Runner in a container][GR]

[GR]: <https://docs.gitlab.com/runner/install/docker.html>
