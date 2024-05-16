Pre-work:

Create Azure Container Registry (Azure Portal)
Create Azure DevOps Service Connection (Azure DevOps/Project Settings/Service Connections) using Service Principal - Automated
Create App Registration
Create secret in App Registration
Create UAT Resource Group
    Create loganalyticsworkspace
    Create appinsights pointed to loganalytics
Create Prod Resource Group
    Create loganalyticsworkspace
    Create appinsights pointed to loganalytics
Create Variable Groups for pipeline (one per desired environment)
    ACRContainerAppId                   gathered from App Registration created above
    appInsightsConnectionString         gathered from App Insights/Properties in the appsinsights instance in the environment's resource group
    AzureLocation                       appropriate Azure location for resources
    containerAppEnvironmentName         arbitrary name for container app environment
    containerAppLogAnalyticsName        gathered from the Overview page of the App Insights instance in the environment's resource group
    containerAppName                    arbitrary name for the container app
    containerAppScaledUpCPU             .5
    containerAppScaledUpMem             1.0
    containerAppScaledUpReplicas        2
    containerRegistryPassword           gathered from App Registrations/Certificates and Secrets
    databaseAction                      Update
    databaseEdition                     Basic
    databaseName                        arbitrary name for Azure SQL database
    databasePassword                    arbitrary password to be set in Azure SQL 
    databasePerformanceLevel            Basic
    databaseUser                        arbitrary user name to be set in Azure SQL 
    environment                         three/four-letter abbreviation for environment name
    httpPort                            8080
    registryLoginServer                 gathered from Azure Container Registry/Overview
    resourceGroupName                   arbitrary name for given resource group, frequently constructed from text-$(environment)
    serviceConnection                   name of the Service Connection created above

