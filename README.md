# Terraform modules

Useful reusable TF modules to use for testing (AWS Core Services).

### Modules 

- [Networking](./networking/README.md)
- [ALB](./alb/README.md)
- **IAM**  
  - [ECR](./iam/ecr/README.md)
  - [ECS](./iam/ecs/README.md)
- **Cloudwatch**   
  - **Alarms:**  
    - [ALB - Http error rate](./cloudwatch/alarms/alb-http-errors/README.md)
    - [Cloudwatch Logs - Application Errors](./cloudwatch/alarms/application-log-errors/README.md)

### Versioning with tags

**Publish tags:**
```sh
git tag -a "v1.0.1" -m "First release of tf modules"
git push origin main --follow-tags
```
**Usage:**

```tf
module "networking" {
  source = "github.com/moabukar/tf-mods//networking?ref=v1.0.1"
}
```
