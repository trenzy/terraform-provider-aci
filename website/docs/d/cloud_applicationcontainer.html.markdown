---
subcategory: "Cloud"
layout: "aci"
page_title: "ACI: aci_cloud_applicationcontainer"
sidebar_current: "docs-aci-data-source-cloud_applicationcontainer"
description: |-
  Data source for Cloud Network Controller Cloud Application container
---

# aci_cloud_applicationcontainer #
Data source for Cloud Network Controller Cloud Application container  
<b>Note: This resource is supported in Cloud Network Controller only. </b>
## Example Usage ##

```hcl
data "aci_cloud_applicationcontainer" "sample_app" {
  tenant_dn  = aci_tenant.dev_tenant.id
  name       = "demo_cloud_app"
}
```
## Argument Reference ##
* `tenant_dn` - (Required) Distinguished name of parent Tenant object.
* `name` - (Required) name of Object cloud_applicationcontainer.



## Attribute Reference

* `id` - Attribute id set to the Dn of the Cloud Application container.
* `description` - (Optional) Description for object cloud applicationcontainer.
* `annotation` - (Optional) Annotation for object cloud applicationcontainer.
* `name_alias` - (Optional) Name alias for object cloud applicationcontainer.
