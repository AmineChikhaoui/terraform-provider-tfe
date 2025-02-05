---
layout: "tfe"
page_title: "Terraform Enterprise: tfe_github_app_installation"
description: |-
Get information on the Github App Installation.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: tfe_github_app_installation

Use this data source to get information about the Github App Installation.

## Example Usage

### Finding a Github App Installation by its installation ID

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataTfeGithubAppInstallation } from "./.gen/providers/tfe/data-tfe-github-app-installation";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new DataTfeGithubAppInstallation(this, "gha_installation", {
      installationId: 12345,
    });
  }
}

```

### Finding a Github App Installation by its name

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataTfeGithubAppInstallation } from "./.gen/providers/tfe/data-tfe-github-app-installation";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new DataTfeGithubAppInstallation(this, "gha_installation", {
      name: "installation_name",
    });
  }
}

```

## Argument Reference

The following arguments are supported. At least one of `name`, `installationId` must be set. 

* `installationId` - (Optional) ID of the Github Installation as shown in Github.
* `name` - (Optional) Name of the Github Installation as shown in Github.
 
Must be one of: `installationId` or `name`.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `id` - The internal ID of the Github Installation. This is different from the `installationId`.
<!-- cache-key: cdktf-0.18.0 input-0a4ff055d60c44b213a5dc7ce9fcb8c10208e9d24cd4e44f3a552a718ea64d50 -->