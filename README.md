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

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
