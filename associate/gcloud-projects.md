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


