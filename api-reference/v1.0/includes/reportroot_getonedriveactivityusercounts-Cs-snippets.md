
```Cs

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var report = await graphClient.Reports.GetOneDriveActivityUserCounts('D7')
    .Request()
    .GetAsync();

```