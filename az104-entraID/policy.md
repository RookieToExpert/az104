## Initiatives
An initiative (sometimes called a policy set) lets you **bundle all those individual rules into one package**.

#### Built-in initiatives
come **ready-made from Microsoft**for common scenarios (like certain compliance standards).
#### Custom initiatives
are ones you **create yourself** by grouping your own custom policies or mixing them with built-in policies.

## Definitions
1. The definition of plicy or initiatives(Json)
2. **Definition location:** This location determines the **scope** to which the initiative or policy **can be assigned**. The location should be the resource container shared by a**ll resources that you want to use the policy definition on**.

## Assignments
1. Policy assignments determine **which resources get evaluated by a policy or initiative.**
2. They let you **choose the scope** (like a management group, subscription, or resource group) so that only certain resources are affected. 
3. You can also **set parameters, overrides, or exclusions**, giving you fine-grained control over exactly how and where each policy is enforced.

## Exemptions
Use the Policy exemptions feature to **exempt a resource** hierarchy or an individual resource from evaluation of initiatives or definitions.

## Evaluation
Azure Policy automatically checks if resources are compliant whenever certain events occur, such as when a policy or initiative is **newly assigned or updated**, or when a **resource is created**, **changed, or deleted**. You can also trigger an on-demand scan if needed. This ensures resources remain compliant throughout their lifecycle.