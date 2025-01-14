---
subcategory: "Cloud"
layout: "aci"
page_title: "ACI: aci_cloud_availability_zone"
sidebar_current: "docs-aci-data-source-cloud_availability_zone"
description: |-
  Data source for Cloud Network Controller Cloud Availability Zone
---

# aci_cloud_availability_zone #
Data source for Cloud Network Controller Cloud Availability Zone  
<b>Note: This resource is supported in Cloud Network Controller only.</b>
## Example Usage ##

```hcl
data "aci_cloud_availability_zone" "az_us_east_1_aws" {
  cloud_providers_region_dn  = aci_cloud_providers_region.region_aws.id
  name                       = "us-east-1a"
}
```
## Argument Reference ##
* `cloud_providers_region_dn` - (Required) Distinguished name of parent CloudProvidersRegion object.
* `name` - (Required) Name of Object cloud availability zone.



## Attribute Reference

* `id` - Attribute id set to the Dn of the Cloud Availability Zone.
* `annotation` - (Optional) Annotation for object cloud availability zone.
* `name_alias` - (Optional) Name alias for object cloud availability zone.
