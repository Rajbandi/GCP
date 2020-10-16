# GCloud Shell command

* Command wide flags
	> gcloud GROUP | COMMAND [--account=ACCOUNT] [--billing-project=BILLING_PROJECT] [--configuration=CONFIGURATION] [--flags-file=YAML_FILE] [--flatten=[KEY,…]] [--format=FORMAT] [--help] [--project=PROJECT_ID] [--quiet, -q] [--verbosity=VERBOSITY; default="warning"] [--version, -v] [-h] [--impersonate-service-account=SERVICE_ACCOUNT_EMAIL] [--log-http] [--trace-token=TRACE_TOKEN] [--no-user-output-enabled]
	> 
	> **--impersonate-service-account**=SERVICE_ACCOUNT_EMAIL
	> 
	> For this gcloud invocation, all API requests will be made as the given service account instead of the currently selected account. This is done without needing to create, download, and activate a key for the account. In order to perform operations as the service account, your currently selected account must have an IAM role that includes the iam.serviceAccounts.getAccessToken permission for the service account. The roles/iam.serviceAccountTokenCreator role has this permission or you may create a custom role. Overrides the default auth/impersonate_service_account property value for this command invocation.

	> **--log-http**

	>Log all HTTP server requests and responses to stderr. Overrides the default core/log_http property value for this command invocation.
	>
	> **--trace-token**=TRACE_TOKEN
	> 
	> Token used to route traces of service requests for investigation of issues. Overrides the default core/trace_token property value for this command invocation.

	> **--billing-project**=BILLING_PROJECT
	> 
	> The Google Cloud Platform project that will be charged quota for operations performed in gcloud. If you need to operate on one project, but need quota against a 	different project, you can use this flag to specify the billing project. If both billing/quota_project and --billing-project are specified, --billing-project takes precedence. 

## Cheat Sheet

[Cheat Sheet](https://cloud.google.com/sdk/gcloud/reference/cheat-sheet)

## Initialization, Active configuration, Named configurations

[Configurations](./gcloud-config.md)

## IAM Roles, Service Accounts, Identity Groups, Memberships

[IAM Roles, Service Accounts, Groups, Memberships](./gcloud-iam.md)

## OAUTH2 (API, Accounts)

[OAuth2](./gcloud-oauth.md)

## Organisations, Projects, Services

[Organisations, Projects, Services](./gcloud-projects.md)
