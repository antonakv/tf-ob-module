# sample repo - create code that can be used as module (gh repo)

## Intro

This manual explains how to use terraform module

Tested on Mac OS X.

## Requirements

- Hashicorp terraform recent version installed
[Terraform installation manual](https://learn.hashicorp.com/tutorials/terraform/install-cli)

- git installed
[Git installation manual](https://git-scm.com/download/mac)

## How to use module
- In order to use module add to main.tf root file following statement
```bash
module "mymodule" {
    source = "github.com/antonakv/tf-ob-module/mymodule"
}
```

