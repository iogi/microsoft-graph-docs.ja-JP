---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 8025766dbf582f59bdcb7dea41fb08d8cf80d72a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527491"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getOneDriveActivityFileCounts(period='D7')?$format=application/json"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *siteActivitySummaryList = [[NSMutableArray alloc] init];
        siteActivitySummaryList = [jsonFinal valueForKey:@"value"];
        MSGraphSiteActivitySummary *siteActivitySummary = [[MSGraphSiteActivitySummary alloc] initWithDictionary:[siteActivitySummaryList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```