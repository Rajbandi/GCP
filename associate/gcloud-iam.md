
## GCloud shell commands for IAM

### Roles

* **Grantable roles**

This command displays the list of grantable roles for a resource. The resource can be referenced either via the full resource name or via a URI. User can then add IAM policy bindings to grant the roles.

> List IAM grantable roles for a resource
> 
> gcloud iam list-grantable-roles RESOURCE [--filter=EXPRESSION] [--page-size=PAGE_SIZE; default=100] [GCLOUD_WIDE_FLAG …]
>
> gcloud iam list-grantable-roles //cloudresourcemanager.googleapis.com/projects/PROJECT_ID
> 
> gcloud iam list-grantable-roles //compute.googleapis.com/projects/example-project/zones/us-central1-f/instances/example-instance
> 
* **Testable roles**
> List IAM testable permissions for a resource
> 
> gcloud iam list-testable-permissions RESOURCE [--filter=EXPRESSION] [GCLOUD_WIDE_FLAG …]
> 
* **List roles**

Testable permissions mean the permissions that user can add or remove in a role at a given resource. The resource can be referenced either via the full resource name or via a URI.

> List the roles defined at a parent organization or a project
> 
>  gcloud iam roles list [--show-deleted] [--organization=ORGANIZATION     | --project=PROJECT_ID] [--filter=EXPRESSION] [--limit=LIMIT] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]

* Describe role
> Show metadata for a role
> 
> gcloud iam roles describe ROLE_ID [--organization=ORGANIZATION     | --project=PROJECT_ID] [GCLOUD_WIDE_FLAG …]

* Create role
> Create a custom role for a project or an organization
> 
> gcloud iam roles create ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [--file=FILE     | --description=DESCRIPTION --permissions=PERMISSIONS --stage=STAGE --title=TITLE] [GCLOUD_WIDE_FLAG …]
 
 * Update role
 > Update an IAM custom role
 > 
 > gcloud iam roles update ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [--file=FILE] [--add-permissions=ADD_PERMISSIONS --description=DESCRIPTION --permissions=PERMISSIONS --remove-permissions=REMOVE_PERMISSIONS --stage=STAGE --title=TITLE] [GCLOUD_WIDE_FLAG …]
 
 * Delete role
 > Delete a custom role from an organization or a project
 > 
 > gcloud iam roles delete ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [GCLOUD_WIDE_FLAG …]

* Copy role
> Create a role from an existing role
> 
> gcloud iam roles copy [--dest-organization=DEST_ORGANIZATION] [--dest-project=DEST_PROJECT] [--destination=DESTINATION] [--source=SOURCE] [--source-organization=SOURCE_ORGANIZATION] [--source-project=SOURCE_PROJECT] [GCLOUD_WIDE_FLAG …]

* Undelete role
> Undelete a custom role from an organization or a project
> 
> gcloud iam roles undelete ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [GCLOUD_WIDE_FLAG …]

### Service Accounts, Policies, Keys

#### Policies
* Get IAM Policy
> Get the IAM policy for a service account
> 
> gcloud iam service-accounts get-iam-policy SERVICE_ACCOUNT [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
> 
* Set IAM Policy
> Set IAM policy for a service account
> 
> gcloud iam service-accounts set-iam-policy SERVICE_ACCOUNT POLICY_FILE [GCLOUD_WIDE_FLAG …]
> 
* Add IAM Policy Binding
> Add an IAM policy binding to an IAM service account
>  
>  gcloud iam service-accounts add-iam-policy-binding SERVICE_ACCOUNT --member=MEMBER --role=ROLE [--condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]
>   
* Remove IAM Policy Binding
> Remove IAM policy binding from a service account
>  
>  gcloud iam service-accounts remove-iam-policy-binding SERVICE_ACCOUNT --member=MEMBER --role=ROLE [--all     | --condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]
>   
#### Service Accounts
Create and manipulate IAM service accounts. A service account is a special Google account that belongs to your application or a VM, instead of to an individual end user. Your application uses the service account to call the Google API of a service, so that the users aren't directly involved.

* List Service Accounts
> List all of a project's service accounts
>  
>  gcloud iam service-accounts list [--filter=EXPRESSION] [--limit=LIMIT] [--sort-by=[FIELD,…]] [--uri] [GCLOUD_WIDE_FLAG …]
>   
* Describe Service Account
> Show metadata for a service account from a project
>  
>  gcloud iam service-accounts describe SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
>   
* Create a Service Account
> Create a service account for a project
>  
>  gcloud iam service-accounts create NAME [--description=DESCRIPTION] [--display-name=DISPLAY_NAME] [GCLOUD_WIDE_FLAG …]
>   
* Update a Service Account
> Update an IAM service account
>  
>  gcloud iam service-accounts update SERVICE_ACCOUNT [--description=DESCRIPTION] [--display-name=DISPLAY_NAME] [GCLOUD_WIDE_FLAG …]
>   
* Delete a Service Account
> Delete a service account from a project
>  
>  gcloud iam service-accounts delete SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
>   
* Enable a Service Account
> Enable an IAM service account
>  
>  gcloud iam service-accounts enable SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
>   
* Disable a Service Account
> Disable an IAM service account
>  
> gcloud iam service-accounts disable SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
> 
#### Keys
Manage service account keys

* List
> List the keys for a service account
>  
>  gcloud iam service-accounts keys list --iam-account=IAM_ACCOUNT [--created-before=CREATED_BEFORE] [--managed-by=MANAGED_BY; default="any"] [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [--uri] [GCLOUD_WIDE_FLAG …]
>   
* Create a key
> Create a private key for a service account
>  
>  gcloud iam service-accounts keys create OUTPUT-FILE --iam-account=IAM_ACCOUNT [--key-file-type=KEY_FILE_TYPE; default="json"] [GCLOUD_WIDE_FLAG …]
> 
* Upload a key
> Upload a public key for an IAM service account
>  
>  gcloud iam service-accounts keys upload PUBLIC_KEY_FILE --iam-account=IAM_ACCOUNT [GCLOUD_WIDE_FLAG …]
>    
* Delete a key
> Delete a user-managed key from a service account
>  
>  gcloud iam service-accounts keys delete KEY-ID --iam-account=IAM_ACCOUNT [GCLOUD_WIDE_FLAG …]
>  
* Sign a blob
> Sign a blob with a managed service account key
>  
>  gcloud iam service-accounts sign-blob INPUT-FILE OUTPUT-FILE --iam-account=IAM_ACCOUNT [GCLOUD_WIDE_FLAG …]
>   

### Identity groups

Commands for managing Cloud Identity Groups.

* Create a new group.

> gcloud identity groups create EMAIL --labels=LABELS (--customer=CUSTOMER     | --organization=ORGANIZATION) [--description=DESCRIPTION] [--display-name=DISPLAY_NAME] [--with-initial-owner=WITH_INITIAL_OWNER] [GCLOUD_WIDE_FLAG …]
> 

* Describe a group

> gcloud identity groups describe EMAIL [GCLOUD_WIDE_FLAG …]
>

* Update a group

> gcloud identity groups update EMAIL [--clear-description     | --description=DESCRIPTION] [--clear-display-name     | --display-name=DISPLAY_NAME] [GCLOUD_WIDE_FLAG …]

* Search a group

> gcloud identity groups search --labels=LABELS (--customer=CUSTOMER     | --organization=ORGANIZATION) [--page-size=PAGE_SIZE] [--page-token=PAGE_TOKEN] [--view=VIEW; default="basic"] [GCLOUD_WIDE_FLAG …]
> 

* Delete a group

> gcloud identity groups delete EMAIL [GCLOUD_WIDE_FLAG …]
>

### Identity Group Memberships

Commands for managing Cloud Identity Groups Memberships.

* List memberships
  
> gcloud identity groups memberships list --group-email=GROUP_EMAIL [--page-token=PAGE_TOKEN] [--view=VIEW; default="basic"] [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
> 

* Describe a membership

> gcloud identity groups memberships describe --group-email=GROUP_EMAIL --member-email=MEMBER_EMAIL [GCLOUD_WIDE_FLAG …]
> 

* Add a membership to group

> gcloud identity groups memberships add --group-email=GROUP_EMAIL --member-email=MEMBER_EMAIL [--roles=[ROLES,…]] [GCLOUD_WIDE_FLAG …]
> 

* Modify membership roles

> Add/remove/modify membership roles OR update expiry details of membership in a group.

> gcloud identity groups memberships modify-membership-roles --group-email=GROUP_EMAIL --member-email=MEMBER_EMAIL [--add-roles=ADD_ROLES --remove-roles=[REMOVE_ROLES,…]] [GCLOUD_WIDE_FLAG …]
> 

* Delete membership from group

> gcloud identity groups memberships delete --group-email=GROUP_EMAIL --member-email=MEMBER_EMAIL [GCLOUD_WIDE_FLAG …]
> 



