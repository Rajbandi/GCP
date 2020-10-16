### Initialization And Configuration
#### Info
Display information about the current gcloud environment.
> gcloud info [--anonymize] [--run-diagnostics     | --show-log] [GCLOUD_WIDE_FLAG …]

#### Initialization
gcloud init launches an interactive Getting Started workflow for the gcloud command-line tool. It performs the following setup steps:

-   Authorizes gcloud and other SDK tools to access Google Cloud Platform using your user account credentials, or from an account of your choosing whose credentials are already available.
-  Sets up a new or existing configuration.
-  Sets properties in that configuration, including the current project and optionally, the default Google Compute Engine region and zone you'd like to use.
gcloud init can be used for initial setup of gcloud and to create new or reinitialize gcloud configurations.

Properties set by gcloud init are local and persistent, and are not affected by remote changes to the project. For example, the default Compute Engine zone in your configuration remains stable, even if you or another user changes the project-level default zone in the Cloud Platform Console.

> gcloud init
> 
#### Active Configuration

The gcloud config command group lets you set, view and unset properties used by Cloud SDK.
A configuration is a set of properties that govern the behavior of gcloud and other Cloud SDK tools. 

* List active configuration
> gcloud config list lists all properties of the active configuration. These include the account used to authorize access to the Cloud Platform, the current Cloud Platform project, and the default Compute Engine region and zone,
>  
>  gcloud config list [SECTION/PROPERTY] [--all] [--filter=EXPRESSION] [--limit=LIMIT] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
>   
* Set configuration property
> gcloud config set sets the specified property in your active configuration only. To set the property across all configurations, use the --installation flag. 
>  
>  gcloud config set SECTION/PROPERTY VALUE [--installation] [GCLOUD_WIDE_FLAG …]
>   
* Get configuration property value
> gcloud config get-value prints the property value from your active client side configuration only.
>  
>  gcloud config get-value SECTION/PROPERTY [GCLOUD_WIDE_FLAG …]
>   
* Unset configuration property
> By default, unsets the property in your active configuration only. Use the `--installation` flag to unset the property across all configurations.
>  
>  gcloud config unset SECTION/PROPERTY [--installation] [GCLOUD_WIDE_FLAG …]

#### Named Configurations

* List of named configurations
> Lists existing named configurations.
>  
>  gcloud config configurations list [--filter=EXPRESSION] [--limit=LIMIT] [--sort-by=[FIELD,…]] [GCLOUD_WIDE_FLAG …]
>  
* Describe a named configuration
> Describes a named configuration by listing its properties.
>  
>  gcloud config configurations describe CONFIGURATION_NAME [--all] [GCLOUD_WIDE_FLAG …]
>  
* Create a new named configuration
> Creates a new named configuration.
>  
>  gcloud config configurations create CONFIGURATION_NAME [--no-activate] [GCLOUD_WIDE_FLAG …]
>  
* Active a named configuration
> Activates an existing named configuration.
>  
>  gcloud config configurations activate CONFIGURATION_NAME [GCLOUD_WIDE_FLAG …]
>   
* Delete a named configuration
> Deletes a named configuration. You cannot delete a configuration that is active, even when overridden with the --configuration flag. To delete the current active configuration, activate another one.
> 
> gcloud config configurations delete CONFIGURATION_NAMES [CONFIGURATION_NAMES …] [GCLOUD_WIDE_FLAG …]
>  
