## Func start -> Can't determine Project to build. Expected 1 .csproj or .fsproj but found 2
* dotnet add package Microsoft.Azure.Functions.Worker.Sdk --version 1.17.2

## Error performing operation on Blob Storage while running function locally
```
[2024-06-24T08:04:25.456Z] There was an error performing a read operation on the Blob Storage Secret Repository.
[2024-06-24T08:04:25.462Z] Azure.Core: No connection could be made because the target machine actively refused it. (127.0.0.1:10000). System.Net.Http: No connection could be made because the target machine actively refused it. (127.0.0.1:10000). System.Net.Sockets: No connection could be made because the target machine actively refused it.
Value cannot be null. (Parameter 'provider')
```
* Add the following to localhost.settings.json

```
	    "AzureWebJobsSecretStorageType": "files",
```
