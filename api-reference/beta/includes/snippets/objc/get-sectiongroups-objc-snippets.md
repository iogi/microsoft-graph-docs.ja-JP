---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 23ce4812088faade0bf3afb8ff6774df7f9b09c0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485950"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/onenote/sectionGroups/{id}/sectionGroups"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *sectionGroupList = [[NSMutableArray alloc] init];
        sectionGroupList = [jsonFinal valueForKey:@"value"];
        MSGraphSectionGroup *sectionGroup = [[MSGraphSectionGroup alloc] initWithDictionary:[sectionGroupList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```