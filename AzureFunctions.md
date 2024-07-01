# Azure Functions
* [Install Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)
* [Install Func CLI](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=windows%2Cisolated-process%2Cnode-v4%2Cpython-v2%2Chttp-trigger%2Ccontainer-apps&pivots=programming-language-csharp)

## Commands
* Start a new project
```
    func init ProjectName --worker-runtime dotnet-isolated
```
* Create a new function
** Http trigger
```
func new --template "Http Trigger" --name FunctionName
```
** Event grid trigger
```
func new --template "Azure Event Grid trigger" --name ShippingRequested --worker-runtime dotnet --language c# --force
```
* Start function runtime locally
```
func start
```
* Deploy
```
az login
func azure functionapp publish teclearn
```
### Authorization types
* Anonymous
* Function level (API Key)
* User (requires valid Azure Active Directory - AAD token)

### Triggers
* Azure Blob Storage trigger
* Azure Cosmos DB trigger
* Durable Functions activity
* Durable Functions entity (class)
* Durable Functions entity (function)
* Durable Functions Entity HTTP starter
* Durable Functions HTTP starter
* Durable Functions orchestrator
* Azure Event Grid Cloud Event trigger
* Azure Event Grid trigger
* Azure Event Hub trigger
* HTTP trigger
* IoT Hub (Event Hub)
* Kafka output
* Kafka trigger
* Azure Queue Storage trigger
* RabbitMQ trigger
* SendGrid
* Azure Service Bus Queue trigger
* Azure Service Bus Topic trigger
* SignalR negotiate HTTP trigger
* SQL Input Binding
* SQL Output Binding
* SQL Trigger
* Timer trigger
