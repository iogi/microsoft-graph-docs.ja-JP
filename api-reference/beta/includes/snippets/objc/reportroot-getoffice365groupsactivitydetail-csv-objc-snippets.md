---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 519773542d67f34ee338f3728519818ec7479d54
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503487"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getOffice365GroupsActivityDetail(period='D7')?$format=text/csv"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *office365GroupsActivityDetailList = [[NSMutableArray alloc] init];
        office365GroupsActivityDetailList = [jsonFinal valueForKey:@"value"];
        MSGraphOffice365GroupsActivityDetail *office365GroupsActivityDetail = [[MSGraphOffice365GroupsActivityDetail alloc] initWithDictionary:[office365GroupsActivityDetailList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```