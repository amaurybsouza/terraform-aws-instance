# Terraform AWS EC2

This project is a way to provision a basic EC2 with variables on AWS using Terraform CLI.

## Credentials on AWS

Use this [article](https://amaurybsouza.medium.com/terraform-e364f5d31570) to create your credentials at AWS.

## Usage

- Prepare your working directory for other commands:

```hcl
$ terraform init
```
- Show changes required by the current configuration:

```hcl
$ terraform plan
```

- Create or update infrastructure:

```hcl
$ terraform apply
```

- Destroy previously-created infrastructure:

```hcl
$ terraform destroy
```

## Basix Example

- A basic example for provider.tf:

```hcl
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 3.0"
    }
  }
}

provider "aws" {
  region = var.region
}

resource "aws_instance" "tutorials" {
  ami           = var.ami
  instance_type = var.instance_type
}
```

- A basix example for variables .tf:

```hcl
variable "region" {
  description = "define what region"
  default     = "us-east-1"
}

variable "ami" {
  description = "define what AMI"
  default     = "ami-09e67e426f25ce0d7"
}

variable "instance_type" {
  description = "value"
  default     = "t2.micro"
}    
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
