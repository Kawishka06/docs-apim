# Updating WSO2 API Manager

WSO2 introduces [WSO2 Updates](https://updates.docs.wso2.com/en/latest/) , which is a command-line utility that allows you to get the latest updates available for a particular product release. These updates include the latest bug fixes and security fixes that are released by WSO2 after a product version is released. Therefore, you do not need to wait for the next product release to receive these fixes.

## WSO2 Updates 2.0

The WSO2 Updates 2.0 tool allows you to update your currently used product by fetching updates from the server. While updating, you should manually merge updated configuration files or use a tool like Puppet. It is also recommended to store backups of your custom configurations in case you need to restore them later.

For more information, see [Using WSO2 Updates 2.0](https://updates.docs.wso2.com/en/latest/updates/update-tool/)

!!! warning

    **Persisting Index data**

    The indexing related information of WSO2 API Manager is stored in the `<API-M_HOME>/solr/data` directory. Once the data is indexed, it is stored in the `index` directory.
    
    !!! tip
        Before discarding the old API Manager instance,
        
        You must take a backup of the `<API-M_HOME>/solr/data` directory and copy it into the updated API Manager distribution `<API-M_HOME>/solr/data`.
    
    **Persisting WSO2CarbonDB**
    
    To avoid conflicts that can occur during the update process, it is recommended to persist the local H2 databases as well.
    
    !!! tip
        Before discarding the old API Manager instance,

        Take a backup of `<API-M_HOME>/repository/database/WSO2CARBON_DB.h2.db` and replace it in the updated API Manager distribution under `<API-M_HOME>/repository/database`.
         
        If you are using the existing local H2 database for WSO2MetricsDB as well,
         
        Take a backup of `<API-M_HOME>/repository/database/WSO2METRICS_DB.h2.db` and replace it in the updated API Manager distribution under `<API-      M_HOME>/repository/database`.
        
    
    For more information on run time and configuration artifact directories of API Manager refer [Common Runtime and Configuration Artifacts]({{base_path}}/administer/product-configurations/common-runtime-and-configuration-artifacts/) .
