# GCloud Shell command

* Command wide flags
	> 

### Roles

* List roles	
> gcloud iam roles list - list the roles defined at a parent organization or a project
> 
>  gcloud iam roles list [--show-deleted] [--organization=ORGANIZATION     | --project=PROJECT_ID] [--filter=EXPRESSION] [--limit=LIMIT] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]

* Describe role
> gcloud iam roles describe - show metadata for a role
> 
> gcloud iam roles describe ROLE_ID [--organization=ORGANIZATION     | --project=PROJECT_ID] [GCLOUD_WIDE_FLAG …]

* **Create role**
> gcloud iam roles create - create a custom role for a project or an organization
> 
> gcloud iam roles create ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [--file=FILE     | --description=DESCRIPTION --permissions=PERMISSIONS --stage=STAGE --title=TITLE] [GCLOUD_WIDE_FLAG …]
 
 * **Update role**
 > gcloud iam roles update - update an IAM custom role
 > 
 > gcloud iam roles update ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [--file=FILE] [--add-permissions=ADD_PERMISSIONS --description=DESCRIPTION --permissions=PERMISSIONS --remove-permissions=REMOVE_PERMISSIONS --stage=STAGE --title=TITLE] [GCLOUD_WIDE_FLAG …]
 
 * **Delete role**
 > gcloud iam roles delete - delete a custom role from an organization or a project
 > 
 > gcloud iam roles delete ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [GCLOUD_WIDE_FLAG …]

* **Copy role**
> gcloud iam roles copy - create a role from an existing role
> 
> gcloud iam roles copy [--dest-organization=DEST_ORGANIZATION] [--dest-project=DEST_PROJECT] [--destination=DESTINATION] [--source=SOURCE] [--source-organization=SOURCE_ORGANIZATION] [--source-project=SOURCE_PROJECT] [GCLOUD_WIDE_FLAG …]

* **Undelete role**
> gcloud iam roles undelete - undelete a custom role from an organization or a project
> 
> gcloud iam roles undelete ROLE_ID (--organization=ORGANIZATION     | --project=PROJECT_ID) [GCLOUD_WIDE_FLAG …]
