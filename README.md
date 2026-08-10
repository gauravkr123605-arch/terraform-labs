# Terraform Labs 🚀

Terraform, Azure and DevOps practice code.

## 📌 Project Overview

This repository contains my Terraform practice and Azure Infrastructure as Code (IaC) configurations.

In this project, I am learning how to create Azure resources using Terraform.

## 🏗️ Azure Resource Group

This project creates multiple Azure Resource Groups using Terraform `for_each`.

### Terraform Code

```hcl
resource "azurerm_resource_group" "rg" {
  for_each = var.rgs

  name     = each.value.name
  location = each.value.location
}