---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9c95b5c39a5d1d7129423e7bb9186a1bb2b7a835
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495533"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/sites/{site-id}/lists/{list-id}/items/{item-id}/versions"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *listItemVersionList = [[NSMutableArray alloc] init];
        listItemVersionList = [jsonFinal valueForKey:@"value"];
        MSGraphListItemVersion *listItemVersion = [[MSGraphListItemVersion alloc] initWithDictionary:[listItemVersionList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```