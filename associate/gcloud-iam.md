## GCloud shell commands for IAM

### Roles

* **Grantable roles**
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
> List the roles defined at a parent organization or a project
> 
>  gcloud iam roles list [--show-deleted] [--organization=ORGANIZATION     | --project=PROJECT_ID] [--filter=EXPRESSION] [--limit=LIMIT] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]

* **Describe role**
> Show metadata for a role
> 
> gcloud iam roles describe ROLE_ID [--organization=ORGANIZATION     | --project=PROJECT_ID] [GCLOUD_WIDE_FLAG …]

* **Create role**
> Create a custom role for a project or an organization
> 
> gcloud iam roles create ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [--file=FILE     | --description=DESCRIPTION --permissions=PERMISSIONS --stage=STAGE --title=TITLE] [GCLOUD_WIDE_FLAG …]
 
 * **Update role**
 > Update an IAM custom role
 > 
 > gcloud iam roles update ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [--file=FILE] [--add-permissions=ADD_PERMISSIONS --description=DESCRIPTION --permissions=PERMISSIONS --remove-permissions=REMOVE_PERMISSIONS --stage=STAGE --title=TITLE] [GCLOUD_WIDE_FLAG …]
 
 * **Delete role**
 > Delete a custom role from an organization or a project
 > 
 > gcloud iam roles delete ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [GCLOUD_WIDE_FLAG …]

* **Copy role**
> Create a role from an existing role
> 
> gcloud iam roles copy [--dest-organization=DEST_ORGANIZATION] [--dest-project=DEST_PROJECT] [--destination=DESTINATION] [--source=SOURCE] [--source-organization=SOURCE_ORGANIZATION] [--source-project=SOURCE_PROJECT] [GCLOUD_WIDE_FLAG …]

* **Undelete role**
> Undelete a custom role from an organization or a project
> 
> gcloud iam roles undelete ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [GCLOUD_WIDE_FLAG …]

### Service Accounts, Policies, Keys

#### Policies
* **Get IAM Policy**
> Get the IAM policy for a service account
> 
> gcloud iam service-accounts get-iam-policy SERVICE_ACCOUNT [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
> 
* **Set IAM Policy**
> Set IAM policy for a service account
> 
> gcloud iam service-accounts set-iam-policy SERVICE_ACCOUNT POLICY_FILE [GCLOUD_WIDE_FLAG …]
> 
* **Add IAM Policy Binding**
> Add an IAM policy binding to an IAM service account
>  
>  gcloud iam service-accounts add-iam-policy-binding SERVICE_ACCOUNT --member=MEMBER --role=ROLE [--condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]
>   
* **Remove IAM Policy Binding**
> Remove IAM policy binding from a service account
>  
>  gcloud iam service-accounts remove-iam-policy-binding SERVICE_ACCOUNT --member=MEMBER --role=ROLE [--all     | --condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]
>   
#### Service Accounts
* **List Service Accounts**
> List all of a project's service accounts
>  
>  gcloud iam service-accounts list [--filter=EXPRESSION] [--limit=LIMIT] [--sort-by=[FIELD,…]] [--uri] [GCLOUD_WIDE_FLAG …]
>   
* **Describe Service Account**
> Show metadata for a service account from a project
>  
>  gcloud iam service-accounts describe SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
>   
* **Create a Service Account**
> Create a service account for a project
>  
>  gcloud iam service-accounts create NAME [--description=DESCRIPTION] [--display-name=DISPLAY_NAME] [GCLOUD_WIDE_FLAG …]
>   
* **Update a Service Account**
> Update an IAM service account
>  
>  gcloud iam service-accounts update SERVICE_ACCOUNT [--description=DESCRIPTION] [--display-name=DISPLAY_NAME] [GCLOUD_WIDE_FLAG …]
>   
* **Delete a Service Account**
> Delete a service account from a project
>  
>  gcloud iam service-accounts delete SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
>   
* **Enable a Service Account**
> Enable an IAM service account
>  
>  gcloud iam service-accounts enable SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
>   
* **Disable a Service Account**
> Disable an IAM service account
>  
> gcloud iam service-accounts disable SERVICE_ACCOUNT [GCLOUD_WIDE_FLAG …]
> 
#### Keys
Manage service account keys

* **List**
> List the keys for a service account
>  
>  gcloud iam service-accounts keys list --iam-account=IAM_ACCOUNT [--created-before=CREATED_BEFORE] [--managed-by=MANAGED_BY; default="any"] [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [--uri] [GCLOUD_WIDE_FLAG …]
>   
* **Create a key**
> Create a private key for a service account
>  
>  gcloud iam service-accounts keys create OUTPUT-FILE --iam-account=IAM_ACCOUNT [--key-file-type=KEY_FILE_TYPE; default="json"] [GCLOUD_WIDE_FLAG …]
> 
* **Upload a key**
> Upload a public key for an IAM service account
>  
>  gcloud iam service-accounts keys upload PUBLIC_KEY_FILE --iam-account=IAM_ACCOUNT [GCLOUD_WIDE_FLAG …]
>    
* **Delete a key**
> Delete a user-managed key from a service account
>  
>  gcloud iam service-accounts keys delete KEY-ID --iam-account=IAM_ACCOUNT [GCLOUD_WIDE_FLAG …]
>  


