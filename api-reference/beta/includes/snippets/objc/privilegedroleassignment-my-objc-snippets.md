---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 857ca4b90100d5e49e025e3484650ef86b756b72
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526048"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/privilegedRoleAssignments/my"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *privilegedRoleAssignmentList = [[NSMutableArray alloc] init];
        privilegedRoleAssignmentList = [jsonFinal valueForKey:@"value"];
        MSGraphPrivilegedRoleAssignment *privilegedRoleAssignment = [[MSGraphPrivilegedRoleAssignment alloc] initWithDictionary:[privilegedRoleAssignmentList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```