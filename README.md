<img src="https://boxboat.com/2020/02/04/writing-a-custom-terraform-provider/featured.png" alt="Terraform logo" title="Terraform" align="right" height="90" width="180"/>

# AWS Secrets Manager Module


```java
module "secrets-manager-1" {

  source = "lgallard/secrets-manager/aws"

  secrets = {
    secret-1 = {
      description             = "My secret 1"
      recovery_window_in_days = 7
      secret_string           = "This is an example"
    },
    secret-2 = {
      description             = "My secret 2"
      recovery_window_in_days = 7
      secret_string           = "This is another example"
    }
  }

  tags = {
    Owner       = "DevOps team"
    Environment = "dev"
    Terraform   = true

  }
}
```
