---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 245ccc66e4c00d84e239f031822370ead2f38c4d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527573"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/directoryRoles/{id}/scopedMembers"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *scopedRoleMembershipList = [[NSMutableArray alloc] init];
        scopedRoleMembershipList = [jsonFinal valueForKey:@"value"];
        MSGraphScopedRoleMembership *scopedRoleMembership = [[MSGraphScopedRoleMembership alloc] initWithDictionary:[scopedRoleMembershipList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```