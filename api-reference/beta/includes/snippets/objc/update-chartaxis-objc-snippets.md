---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ab2b68a1f719a396f1990ea68dd8501fae623f5b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485836"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueaxis"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphWorkbookChartAxis *workbookChartAxis = [[MSGraphWorkbookChartAxis alloc] init];
MSGraphJson *majorUnit = [[MSGraphJson alloc] init];
[workbookChartAxis setMajorUnit:majorUnit];
MSGraphJson *maximum = [[MSGraphJson alloc] init];
[workbookChartAxis setMaximum:maximum];
MSGraphJson *minimum = [[MSGraphJson alloc] init];
[workbookChartAxis setMinimum:minimum];

NSError *error;
NSData *workbookChartAxisData = [workbookChartAxis getSerializedDataWithError:&error];
[urlRequest setHTTPBody:workbookChartAxisData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```