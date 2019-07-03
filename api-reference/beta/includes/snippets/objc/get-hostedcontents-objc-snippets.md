---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: eda0abba23bfcd2376b7ca8e9b9da1cc1c45a118
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487075"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/chats/{id}/messages/{id}/hostedContents"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *chatMessageHostedContentList = [[NSMutableArray alloc] init];
        chatMessageHostedContentList = [jsonFinal valueForKey:@"value"];
        MSGraphChatMessageHostedContent *chatMessageHostedContent = [[MSGraphChatMessageHostedContent alloc] initWithDictionary:[chatMessageHostedContentList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```