---
layout: "tfe"
page_title: "Terraform Enterprise: tfe_team"
description: |-
  Manages teams.
---


<!-- Please do not edit this file, it is generated. -->
# tfe_team

Manages teams.

## Example Usage

Basic usage:

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { Team } from "./.gen/providers/tfe/team";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new Team(this, "test", {
      name: "my-team-name",
      organization: "my-org-name",
    });
  }
}

```

Organization Permission usage:

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { Team } from "./.gen/providers/tfe/team";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new Team(this, "test", {
      name: "my-team-name",
      organization: "my-org-name",
      organizationAccess: {
        manageVcsSettings: true,
      },
    });
  }
}

```

## Argument Reference

The following arguments are supported:

* `name` - (Required) Name of the team.
* `organization` - (Optional) Name of the organization. If omitted, organization must be defined in the provider config.
* `visibility` - (Optional) The visibility of the team ("secret" or "organization"). Defaults to "secret".
* `organizationAccess` - (Optional) Settings for the team's [organization access](https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/permissions#organization-permissions).
* `ssoTeamId` - (Optional) Unique Identifier to control [team membership](https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/single-sign-on#team-names-and-sso-team-ids) via SAML. Defaults to `null`

The `organizationAccess` block supports:

* `readWorkspaces` - (Optional) Allow members to view all workspaces in this organization.
* `readProjects` - (Optional) Allow members to view all projects within the organization. Requires `readWorkspaces` to be set to `true`.
* `managePolicies` - (Optional) Allows members to create, edit, and delete the organization's Sentinel policies.
* `managePolicyOverrides` - (Optional) Allows members to override soft-mandatory policy checks.
* `manageWorkspaces` - (Optional) Allows members to create and administrate all workspaces within the organization.
* `manageVcsSettings` - (Optional) Allows members to manage the organization's VCS Providers and SSH keys.
* `manageProviders` - (Optional) Allow members to publish and delete providers in the organization's private registry.
* `manageModules` - (Optional) Allow members to publish and delete modules in the organization's private registry.
* `manageRunTasks` - (Optional) Allow members to create, edit, and delete the organization's run tasks.
* `manageProjects` - (Optional) Allow members to create and administrate all projects within the organization. Requires `manageWorkspaces` to be set to `true`.
* `manageMembership` - (Optional) Allow members to add/remove users from the organization, and to add/remove users from visible teams.

## Attributes Reference

* `id` The ID of the team.

## Import

Teams can be imported; use `<ORGANIZATION NAME>/<TEAM ID>` or `<ORGANIZATION NAME>/<TEAM NAME>` as the import ID. For
example:

```shell
terraform import tfe_team.test my-org-name/team-uomQZysH9ou42ZYY
```
or
```shell
terraform import tfe_team.test my-org-name/my-team-name
```

<!-- cache-key: cdktf-0.18.0 input-dc64726d4c7e0673d2977d4ee669481de15489f255f8be717ed7c1c037e736b8 -->