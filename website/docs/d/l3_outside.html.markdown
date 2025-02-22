---
subcategory: "L3Out"
layout: "aci"
page_title: "ACI: aci_l3_outside"
sidebar_current: "docs-aci-data-source-l3_outside"
description: |-
  Data source for ACI L3 Outside
---

# aci_l3_outside #
Data source for ACI L3 Outside

## API Information ##

* `Class` - l3extOut
* `Distinguished Name` - uni/tn-{tenant_name}/out-{l3_outside_name}

## GUI Information ##

* `Location` - Tenant -> Networking -> L3Outs

## Example Usage ##

```hcl
data "aci_l3_outside" "foo_l3_outside" {
  tenant_dn = aci_tenant.terraform_tenant.id
  name      = "foo_l3_outside"
}
```

## Argument Reference ##
* `tenant_dn` - (Required) Distinguished name of the parent Tenant object.
* `name` - (Required) Name of the L3 Outside object.

## Attribute Reference

* `id` - Attribute id set to the Dn of the L3 Outside.
* `description`- (Read-Only) Description of the L3 Outside object.
* `annotation` - (Read-Only) Annotation of the L3 Outside object.
* `enforce_rtctrl` - (Read-Only) Enforce route control type of the L3 Outside object. 
* `name_alias` - (Read-Only) Name alias of the L3 Outside object.
* `target_dscp` - (Read-Only) The target differentiated services code point (DSCP) of the path attached to the L3 Outside object.
* `mpls_enabled` - (Read-Only) Indiscate whether MPLS is enabled or not.
* `pim` - (Read-Only) Multicast Address Families.
* `relation_l3ext_rs_dampening_pol` - (Read-Only) Relation to Route Control Profile for Dampening Policies (class rtctrlProfile). Cardinality - N_TO_M. Type - Block.
  * tn_rtctrl_profile_name - (Deprecated) Name of the Route Control Profile for Dampening Policies.
  * tn_rtctrl_profile_dn - (Read-Only) Distinguished name of the Route Control Profile for Dampening Policies.
  * af - (Read-Only) Address Family of the Dampening Policies.
* `relation_l3ext_rs_ectx` - (Read-Only) Relation to VRF (class fvCtx). Cardinality - N_TO_ONE. Type - String.
* `relation_l3ext_rs_interleak_pol` - (Read-Only) Relation to Route Profile for Interleak (class rtctrlProfile). Cardinality - N_TO_ONE. Type - String.
* `relation_l3ext_rs_l3_dom_att` - (Read-Only) Relation to a L3 Domain (class extnwDomP). Cardinality - N_TO_ONE. Type - String.
* `relation_l3extrs_redistribute_pol` - (Read-Only) A block representing the relation to a Route Profile for Redistribution (class rtctrlProfile). Cardinality - N_TO_M. Type: Block.
  * `source` - (Read-Only) Route Map Source for the Route Profile for Redistribution.
  * `target_dn` - (Read-Only) Distinguished name of the Route Control Profile for the Route Profile for Redistribution.