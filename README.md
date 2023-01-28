# Introduction:

The module is used to deploy azure kubernetes service over terraform with a default setup (Infrastructure as Code).

# Exmaple Use of Modul:

> Requirement: network module

    module "kubernetes" {

        source = "github.com/la-cc/terraform-azure-kubernetes?ref=1.0.0"

        resource_group_name          = module.rg.main.name
        virtual_network_id           = module.network.virtual_network_id
        virtual_network_name         = module.network.virtual_network_name

    }
