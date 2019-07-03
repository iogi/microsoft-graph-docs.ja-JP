---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e7abe19b4d963af597a3eec8a9fd04bd39a7fb89
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513683"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/onenote/notebooks"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *notebookList = [[NSMutableArray alloc] init];
        notebookList = [jsonFinal valueForKey:@"value"];
        MSGraphNotebook *notebook = [[MSGraphNotebook alloc] initWithDictionary:[notebookList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```