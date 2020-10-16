### Organisations

Lets you create and manage Cloud Organizations. Google Cloud Platform resources form a hierarchy with Organizations at the root. Organizations contain projects, and Projects contain the remaining Google Cloud Platform resources.

* List 

> Lists all organizations to which the user has access. Organizations are listed in an unspecified order.
>
> gcloud organizations list [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [--uri] [GCLOUD_WIDE_FLAG …]
> 

* Describe 

> Shows metadata for an organization, given a valid organization ID.
> 
> gcloud organizations describe ORGANIZATION_ID [GCLOUD_WIDE_FLAG …]
> 

#### Policies

* Get IAM policy

> Gets the IAM policy for an organization, given an organization ID.
> 
> gcloud organizations get-iam-policy ORGANIZATION_ID [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
> 

* Set IAM policy

> Given an organization ID and a file encoded in JSON or YAML that contains the IAM policy, this command will set the IAM policy for that organization.
> 
> gcloud organizations set-iam-policy ORGANIZATION_ID POLICY_FILE [GCLOUD_WIDE_FLAG …]
>

* Add IAM policy binding

> Adds a policy binding to the IAM policy of an organization, given an organization ID and the binding. One binding consists of a member, a role, and an optional condition.
> 
> gcloud organizations add-iam-policy-binding ORGANIZATION --member=MEMBER --role=ROLE [--condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]
> 

* Remove IAM policy binding

> Removes a policy binding from the IAM policy of an organization, given an organization ID and the binding. One binding consists of a member, a role, and an optional condition.
> 
> gcloud organizations remove-iam-policy-binding ORGANIZATION --member=MEMBER --role=ROLE [--all     | --condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]
> 


### Projects

The gcloud projects group lets you create and manage IAM policies for projects on the Google Cloud Platform. 

* List 

> Lists all active projects, where the active account has Owner, Editor or Viewer permissions. 
>  
> gcloud projects list [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [--uri] [GCLOUD_WIDE_FLAG …]
>  

* Describe a project

> Shows metadata for a project given a valid project ID.
>  
> gcloud projects describe PROJECT_ID_OR_NUMBER [GCLOUD_WIDE_FLAG …]
>  

* Get Ancestors

> Displays the ancestors for a project.
>  
> gcloud projects get-ancestors PROJECT_ID [GCLOUD_WIDE_FLAG …]
>

* Create a project

> Creates a new project with the given project ID. By default, projects are not created under a parent resource. 
>  
> gcloud projects create [PROJECT_ID] [--no-enable-cloud-apis] [--folder=FOLDER_ID] [--labels=[KEY=VALUE,…]] [--name=NAME] [--organization=ORGANIZATION_ID] [--set-as-default] [GCLOUD_WIDE_FLAG …]
>  

* Update a project

> Update the name of the given project.
>  
> gcloud projects update PROJECT_ID --name=NAME [GCLOUD_WIDE_FLAG …]
> 

* Delete a project

> Deletes the project with the given project ID.
>  
> gcloud projects delete PROJECT_ID_OR_NUMBER [GCLOUD_WIDE_FLAG …]
>  

* Undelete a project

> Undeletes the project with the given project ID.
> 
> gcloud projects undelete PROJECT_ID_OR_NUMBER [GCLOUD_WIDE_FLAG …]
>  


#### Policies

* Get IAM Policy

> Gets the IAM policy for a project, given a project ID.
>  
> gcloud projects get-iam-policy PROJECT_ID_OR_NUMBER [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]

* Set IAM Policy

> Sets the IAM policy for a project, given a project ID and a file encoded in JSON or YAML that contains the IAM policy.
>  
> gcloud projects set-iam-policy PROJECT_ID_OR_NUMBER POLICY_FILE [GCLOUD_WIDE_FLAG …]
> 

* Add IAM Policy binding

> Adds a policy binding to the IAM policy of a project, given a project ID and the binding. One binding consists of a member, a role, and an optional condition.
>  
> gcloud projects add-iam-policy-binding PROJECT_ID --member=MEMBER --role=ROLE [--condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]

> MEMBER should be one of the following :

> - Of the form user|group|serviceAccount:email or domain:domain.

> - **allUsers** - Special identifier that represents anyone who is on the internet, with or without a Google account.
> - **allAuthenticatedUsers** - Special identifier that represents anyone who is authenticated with a Google account or a service account.
> 

* Remove IAM Policy binding

> Removes a policy binding to the IAM policy of a project, given a project ID and the binding. 
> 
> gcloud projects remove-iam-policy-binding PROJECT_ID --member=MEMBER --role=ROLE [--all     | --condition=[KEY=VALUE,…]     | --condition-from-file=CONDITION_FROM_FILE] [GCLOUD_WIDE_FLAG …]
>

* Get Ancestors IAM policy

> Get IAM policies for a project and its ancestors, given a project ID.
> 
> gcloud projects get-ancestors-iam-policy PROJECT_ID [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
>  

### Services

The gcloud services command group lets you manage your project's access to services provided by Google and third parties.

* List

> Lists the services that are enabled or available to be enabled by a project. You can choose the mode in which the command will list services by using exactly one of the --enabled or --available flags. --enabled is the default.
> 
> gcloud services list [--available | --enabled] [--filter=EXPRESSION] [--limit=LIMIT] [--page-size=PAGE_SIZE] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
> 

* Enable

>
> gcloud services enable [SERVICE …] [--async] [GCLOUD_WIDE_FLAG …]
> 

* Disable

> gcloud services disable [SERVICE …] [--async] [--force] [GCLOUD_WIDE_FLAG …]
> 

#### Operations

Manage Operation for various services.

* Describe

> Return information about an operation given the name of that operation.
>  
> gcloud services operations describe OPERATION [--full=FULL] [GCLOUD_WIDE_FLAG …]
> 

* Wait

>  Block until an operation has been marked as complete.
>  
>  gcloud services operations wait OPERATION [GCLOUD_WIDE_FLAG …]
>  

* Peered DNS domains

> Peered DNS domains for various private service connections.
> 
> gcloud services peered-dns-domains [GCLOUD_WIDE_FLAG …]
> 


### Vpc-Peerings

VPC Peerings to various services.

* List

> lists connections of a network to a service via VPC peering for a project.
> 
> gcloud services vpc-peerings list --network=NETWORK [--service=SERVICE] [GCLOUD_WIDE_FLAG …]
>

* Connect

> Connects a private service connection to a service via a VPC network.
>  
> gcloud services vpc-peerings connect --network=NETWORK --ranges=RANGES [--async] [--service=SERVICE; default="servicenetworking.googleapis.com"] [GCLOUD_WIDE_FLAG …]
>

* Update

> updates a private service connection to a service via a VPC network.
> 
> gcloud services vpc-peerings update --network=NETWORK [--async] [--force] [--ranges=RANGES] [--service=SERVICE; default="servicenetworking.googleapis.com"] [GCLOUD_WIDE_FLAG …]
> 

#### Operations

Manage VPC Peering operations.

* Describe

>  Return information about an operation given the name of that operation.
>
> gcloud services vpc-peerings operations describe --name=OPERATION_NAME [GCLOUD_WIDE_FLAG …]
> 

* Wait

> Block until an operation has been marked as complete.
> 
> gcloud services vpc-peerings operations wait --name=OPERATION_NAME [GCLOUD_WIDE_FLAG …]
> 

