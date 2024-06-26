# Azure Web App

## Azure App Service Documentation
### Java and Spring Boot with Gradle
https://learn.microsoft.com/hr-hr/azure/app-service/configure-language-java?pivots=platform-linux#gradle

## Deploying Gradle Spring Boot App
* Locally app can expose any port, azure will automatically remap tomcat to port 80 and be available on azure uri
* Add azure plugin to app plugin list in build.gradle:
```
  id("com.microsoft.azure.azurewebapp") version "1.10.0"
```
https://github.com/microsoft/azure-gradle-plugins/tree/master/azure-webapp-gradle-plugin
* Add plugin azure configuration and fill in app and subscription info (template in above plugin link)
* Make sure that Azure CLI is installed
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli
Login to Azure using "az login" or "az login --use-device-code" which enables login via any device or browser
(not necessarily default) by using temporary code as intermediary.
* Use gradle task to deploy app (login to Azure using CLI first)
```
  gradle azureWebAppDeploy
```
## Azure Container Apps
Documentation:
https://learn.microsoft.com/en-us/azure/container-apps/
