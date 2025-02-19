## user
#### What is a user account:
1. Every user who needs access to Azure resources needs an Azure user account.
2. Once authenticated Microsoft Entra ID builds an **access token** to **authorize** the user and **determine what resources they can access** and what they can do with those resources.

#### Entra ID defines users in three ways:
1. **Cloud identites:** Only exist in Entra ID
2. **Directory-synchronized identities:** Exists on both on-premises AD and Entra ID(sync from AD via **Microsoft Entra Connect**)
3.**Guest users:** Exist outside Azures such as other cloud providers, they are **invited users**.


## group
Using groups lets the resource owner **assign** a set of access permissions to **all the members of the group**.

#### Entra ID allows you to define two different types of groups
1. **Security groups**: common group. For ex, you can create a security group for **a specific security policy**, instead of having to add permissions to each member individually. This option requires a **Microsoft Entra administrator.**
2. **Microsoft 365 groups**:
provide collaboration opportunities by giving members **access to a shared mailbox**, calendar, files, SharePoint site, and more.

#### How members are added to the group:
1. **Assigned** - members are added and maintained manually.
2. **Dynamic** - members are added based on rules, creating a Dynamic Group. These groups are still either a security group or Microsoft 365 group, just their members are controlled by rule.