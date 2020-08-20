###Design Principal:
  - Implement a strong identity foundation
  
  - Enable traceability
  - Apply security at all layers
  - Automate security best practices
  - Protect data in transit and at rest
  - Prepare for security events

Defintion:
  - Indentity and Access Managenment
    - Protecting AWS Credentials: 
      - MFA for Root Account
      - MFA for critical API Call (`S3 delete can using MFA`) 
      - IAM
      - IAM instance profiles for EC2 instances
      - AWS STS
      - `Rotate Access Key if want to continue to use, if no can use IAM role to grant S3`
    - Fine-grained authorization
      - IAM, IAM Role
      - AWS Organtizations
  - Detective Controls
  - Infrastructure Protection
    - System Manager(`Session manager`)
  - Data Protection
    
- IAM role to access s3
##### public key to all aws machine
