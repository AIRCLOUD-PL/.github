<p align="center">
  <img src="banner.png" alt="AIRCLOUD — Folding AI into an organisation that actually works." width="100%" />
</p>

# AIRCLOUD

**AI and DevOps to production** — Azure, AWS, GCP and on-prem. Founded and run by [Łukasz Kołodziej](https://github.com/lkolo-prez), AI Infrastructure & DevOps Engineer.

> Most AI projects stop at the demo. We build the infrastructure and the engineering process that take them to production.

[aircloud.com.pl](https://aircloud.com.pl) · [About](https://aircloud.com.pl/en/about) · [Insights](https://aircloud.com.pl/en/knowledge) · [LinkedIn](https://www.linkedin.com/in/lukasz-kolodziej/) · B2B, 100% remote

## Azure Terraform modules

Parameterised, production-oriented Terraform modules for Azure (`azurerm` 4.x, Terraform ≥ 1.5). Every module passes `terraform fmt` and `validate` in CI; Trivy and Checkov results are published in each repository's Security tab.

| Area | Modules |
|---|---|
| Foundation | [resource-group](https://github.com/AIRCLOUD-PL/azure-resource-group-module) · [rbac-management](https://github.com/AIRCLOUD-PL/azure-rbac-management) · [multi-tenant-config](https://github.com/AIRCLOUD-PL/azure-multi-tenant-config) · [key-vault](https://github.com/AIRCLOUD-PL/azure-key-vault-module) |
| Networking | [virtual-network](https://github.com/AIRCLOUD-PL/azure-virtual-network-module) · [network-interface](https://github.com/AIRCLOUD-PL/azure-network-interface-module) · [nsg-firewall](https://github.com/AIRCLOUD-PL/azure-nsg-firewall-module) · [firewall](https://github.com/AIRCLOUD-PL/azure-firewall-module) · [application-gateway](https://github.com/AIRCLOUD-PL/azure-application-gateway-module) · [front-door](https://github.com/AIRCLOUD-PL/azure-front-door-module) · [vpn-gateway](https://github.com/AIRCLOUD-PL/azure-vpn-gateway-module) · [expressroute](https://github.com/AIRCLOUD-PL/azure-expressroute-module) |
| Compute & containers | [aks](https://github.com/AIRCLOUD-PL/azure-aks-module) · [virtual-machine](https://github.com/AIRCLOUD-PL/azure-virtual-machine-module) |
| Data | [storage-account](https://github.com/AIRCLOUD-PL/azure-storage-account-module) · [sql-database](https://github.com/AIRCLOUD-PL/azure-sql-database-module) · [cosmos-db](https://github.com/AIRCLOUD-PL/azure-cosmos-db-module) · [databricks](https://github.com/AIRCLOUD-PL/azure-databricks-module) · [synapse](https://github.com/AIRCLOUD-PL/azure-synapse-module) |
| Integration | [api-management](https://github.com/AIRCLOUD-PL/azure-api-management-module) · [service-bus](https://github.com/AIRCLOUD-PL/azure-service-bus-module) · [event-hubs](https://github.com/AIRCLOUD-PL/azure-event-hubs-module) |
| Examples | [infrastructure-examples](https://github.com/AIRCLOUD-PL/azure-infrastructure-examples) — multi-environment configurations built from the modules |

Use a module straight from GitHub:

```hcl
module "key_vault" {
  source = "git::https://github.com/AIRCLOUD-PL/azure-key-vault-module.git?ref=main"
  # ...
}
```

More golden-path templates (GitOps, Terraform on Azure, backend and frontend services): [github.com/lkolo-prez](https://github.com/lkolo-prez).

---

**Have an AI prototype that needs to reach production?** [Get in touch](https://aircloud.com.pl/en/contact).
