---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9a16d416db14e5907dc9b1bd4f8f3cde82085bd4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526646"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getOffice365ActivationsUserCounts?$format=application/json"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *office365ActivationsUserCountsList = [[NSMutableArray alloc] init];
        office365ActivationsUserCountsList = [jsonFinal valueForKey:@"value"];
        MSGraphOffice365ActivationsUserCounts *office365ActivationsUserCounts = [[MSGraphOffice365ActivationsUserCounts alloc] initWithDictionary:[office365ActivationsUserCountsList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```