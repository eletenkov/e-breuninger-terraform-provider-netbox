---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "netbox_ip_range Data Source - terraform-provider-netbox"
subcategory: ""
description: |-
  
---

# netbox_ip_range (Data Source)

Per [the docs](https://netbox.readthedocs.io/en/stable/models/ipam/iprange/):

> An IP Range object in NetBox represents an arbitrary range of individual IPv4 or IPv6 addresses, inclusive of its starting and ending addresses. For instance, the range 192.0.2.10 to 192.0.2.20 has eleven members. (The total member count is available as the size property on an IPRange instance.) Like prefixes and IP addresses, each IP range may optionally be assigned to a VRF and/or tenant.

## Example Usage

```terraform
data "netbox_ip_range" "cust-a-prod" {
    contains = "10.0.0.1/24"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **contains** (String) CIDR within range you want to retrieve

### Optional

- **id** (String) The ID of this resource.

