---
subcategory: "VPC (Virtual Private Cloud)"
layout: "aws"
page_title: "AWS: aws_vpc_dhcp_options_association"
description: |-
  Provides a VPC DHCP Options Association resource.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_vpc_dhcp_options_association

Provides a VPC DHCP Options Association resource.

## Example Usage

```python
# Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import Token, TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.vpc_dhcp_options_association import VpcDhcpOptionsAssociation
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        VpcDhcpOptionsAssociation(self, "dns_resolver",
            dhcp_options_id=foo.id,
            vpc_id=Token.as_string(aws_vpc_foo.id)
        )
```

## Argument Reference

The following arguments are supported:

* `vpc_id` - (Required) The ID of the VPC to which we would like to associate a DHCP Options Set.
* `dhcp_options_id` - (Required) The ID of the DHCP Options Set to associate to the VPC.

## Remarks

* You can only associate one DHCP Options Set to a given VPC ID.
* Removing the DHCP Options Association automatically sets AWS's `default` DHCP Options Set to the VPC.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `id` - The ID of the DHCP Options Set Association.

## Import

DHCP associations can be imported by providing the VPC ID associated with the options:

```
$ terraform import aws_vpc_dhcp_options_association.imported vpc-0f001273ec18911b1
```

<!-- cache-key: cdktf-0.17.1 input-a700e608592d667c741c37ae143b6b79c2e9d2b180f00f29a4c08f8fd7c60bb6 -->