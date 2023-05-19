---
# generated by https://github.com/fbreckle/terraform-plugin-docs
page_title: "netbox_vlan_group Resource - terraform-provider-netbox"
subcategory: "IP Address Management (IPAM)"
description: |-
  A VLAN Group represents a collection of VLANs. Generally, these are limited by one of a number of scopes such as "Site" or "Virtualization Cluster".
---

# netbox_vlan_group (Resource)

> A VLAN Group represents a collection of VLANs. Generally, these are limited by one of a number of scopes such as "Site" or "Virtualization Cluster".

## Example Usage

```terraform
#Basic VLAN Group example
resource "netbox_vlan_group" "example1" {
  name    = "example1"
  slug    = "example1"
  min_vid = 1
  max_vid = 4094
}

#Full VLAN Group example
resource "netbox_vlan_group" "example2" {
  name        = "Second Example"
  slug        = "example2"
  min_vid     = 1
  max_vid     = 4094
  scope_type  = "dcim.site"
  scope_id    = netbox_site.example.id
  description = "Second Example VLAN Group"
  tags        = [netbox_tag.example.id]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `max_vid` (Number)
- `min_vid` (Number)
- `name` (String)
- `slug` (String)

### Optional

- `description` (String) Defaults to `""`.
- `scope_id` (Number)
- `scope_type` (String)
- `tags` (Set of String)

### Read-Only

- `id` (String) The ID of this resource.

