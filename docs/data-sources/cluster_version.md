---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "ocp_cluster_version Data Source - terraform-provider-ocp"
subcategory: ""
description: |-
  List available cluster versions and images for Kubernetes Cluster.
---

# ocp_cluster_version

List available cluster versions and images for Kubernetes Cluster.

## Example Usage

```hcl
data "ocp_cluster_version" "list_versions" {
  filter {
    version = "v1.27.4"
  }
}
```

## Argument Reference

- `filter` - (Optional) Values to filter available versions and images:
    + `version` - (String) Filter by kubernetes version
    + `os_distro` - (String) Filter by OS Distro. (Ubuntu etc..)
    + `image_name` - (String) Filter by image system full name.

## Attributes Reference

- `versions` - List of Cluster Version objects
    * `id` - (String)
    * `version` - (String) Version cluster (`v1.27.4`)
    * `images` - List of Images Objects
        + `image_name` - (String) Image system name 
        + `name` - (String) Image Name
        + `openstack_id` - (String) Image id in Openstack
        + `os_distro` - (String) Image OS Distro






  







