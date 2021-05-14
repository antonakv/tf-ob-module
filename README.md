# sample repo - create code that can be used as module (gh repo)

## Intro

This manual is dedicated to run terraform code with module

Tested on Mac OS X.

## Requirements

- Hashicorp terraform recent version installed
[Terraform installation manual](https://learn.hashicorp.com/tutorials/terraform/install-cli)

- git installed
[Git installation manual](https://git-scm.com/download/mac)

## Preparation 
- Clone git repository. 

```bash
git clone https://github.com/antonakv/tf-ob-module.git
```

Expected command output looks like this:

```bash
Cloning into 'tf-ob-module'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 12 (delta 1), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (12/12), done.
Resolving deltas: 100% (1/1), done.
```

- Change folder to tf-ob-module

```bash
cd tf-ob-module
```

## Run terraform code

- In the same folder you were before run init

```bash
terraform init
```

Sample result
```bash
$ terraform init

Initializing the backend...

Initializing provider plugins...
- Finding latest version of hashicorp/null...
- Installing hashicorp/null v3.1.0...
- Installed hashicorp/null v3.1.0 (self-signed, key ID 34365D9472D7468F)

Partner and community providers are signed by their developers.
If you d like to know more about provider signing, you can read about it here:
https://www.terraform.io/docs/cli/plugins/signing.html

Terraform has created a lock file .terraform.lock.hcl to record the provider
selections it made above. Include this file in your version control repository
so that Terraform can guarantee to make the same selections by default when
you run "terraform init" in the future.

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.

```

- Run `terraform apply`

Sample result
```bash
$ terraform apply

An execution plan has been generated and is shown below.
Resource actions are indicated with the following symbols:
  + create

Terraform will perform the following actions:

  # null_resource.mynull[0] will be created
  + resource "null_resource" "mynull" {
      + id = (known after apply)
    }

  # null_resource.mynull[1] will be created
  + resource "null_resource" "mynull" {
      + id = (known after apply)
    }

Plan: 2 to add, 0 to change, 0 to destroy.

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: yes

null_resource.mynull[1]: Creating...
null_resource.mynull[0]: Creating...
null_resource.mynull[0]: Creation complete after 0s [id=5957131771339886286]
null_resource.mynull[1]: Creation complete after 0s [id=1742370409598221831]

Apply complete! Resources: 2 added, 0 changed, 0 destroyed.

```
