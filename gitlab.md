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



# Reference
[Run GitLab Runner in a container][GR]
```sh
$ touch /etc/docker/daemon.json 
```
```json
{
    "insecure-registries" : ["registry.gitlab.kronostoken.com"]
}
```




[GR]: <https://docs.gitlab.com/runner/install/docker.html>
