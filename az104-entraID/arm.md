## Hierarchy for governance
Azure provides four levels of management to establish proper governance: **Management groups**, **Subscriptions**, **Resource groups**, and **Resources**

![0](/img/1-entraID/Capture.PNG)

## ARM(Azure Resource Manager)

**Azure Resource Manager** is the **deployment and management service** for Azure. It provides a management layer that allows you to create, update, and delete resources in your Azure account.

## control plane and data plane
The **control plane** helps you **manage resources** in your subscription, while the **data plane** allows you to **access the capabilities** provided by instances of specific resource types.

![0](/img/1-entraID/Capture1.PNG)

#### Control plane
1. When you send a control plane request through **any of**the Azure APIs, tools, or SDKs, **Azure Resource Manager receives the request**. 
2. These tools **use the same API to process requests**, ensuring uniform results and capabilities. 
3. The Resource Manager **authenticates and authorizes** the request before forwarding it to the **appropriate Azure resource provider** that completes the operation.

#### Data plane
1. Data plane operations **aren't limited to REST API**. 
2. Requests are made **directly to the data endpoints of services** (for example, accessing data in Microsoft Azure Storage, querying an SQL database, or reading secrets from Microsoft Azure Key Vault).
3. Each Azure service handles these requests internally, **bypassing Azure Resource Manager**, and directly managing the data through its resource provider. 
4. Service-specific access controls, such as **RBAC or access control lists (ACLs)**, often manage **data plane permissions**. The service responds with the data or result of the data operation, ensuring that the requester has the correct permissions.
5. Azure Policy allows individual Azure services to **implement an Azure Policy extension**, enhancing policy behavior and integration with specific resource providers.

## Operations flow of ARM

![0](/img/1-entraID/Capture2.PNG)

#### Greenfield
Greenfield refers to a scenario where **an Azure Policy (policy-first) exists**, and when you're creating or updating an Azure resource.

#### Brownfield
Brownfield is the scenario where the **resources exist already (resource-first)**, and you're assigning a new Azure Policy to those resources.

You can create an Azure policy that **prohibits resources from** being created outside of a certain region, such as **West Europe**. 
Existing resources outside this region **aren't deleted but are flagged as noncompliant** after the policy is applied, and future attempts to create resources outside West Europe fail.