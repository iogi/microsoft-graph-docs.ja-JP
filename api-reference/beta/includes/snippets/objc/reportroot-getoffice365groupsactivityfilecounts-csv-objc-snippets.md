---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a05623e1c8e52c41e8f8236c838da8a63ea2002a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486132"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getOffice365GroupsActivityFileCounts(period='D7')?$format=text/csv"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *office365GroupsActivityFileCountsList = [[NSMutableArray alloc] init];
        office365GroupsActivityFileCountsList = [jsonFinal valueForKey:@"value"];
        MSGraphOffice365GroupsActivityFileCounts *office365GroupsActivityFileCounts = [[MSGraphOffice365GroupsActivityFileCounts alloc] initWithDictionary:[office365GroupsActivityFileCountsList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```