---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 658b762003a208cbc6b49548faba4cba0016c8c0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486312"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/groups/c75831bdfad/threads/AAQkAGF97XEKhULw/posts/AAMkAGFcAAA/attachments"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphAttachment *attachment = [[MSGraphAttachment alloc] init];
[attachment setName:@"Personal pictures"];
[attachment setSourceUrl:@"https://contoso.com/personal/mario_contoso_net/Documents/Pics"];
[attachment setProviderType:@"oneDriveConsumer"];
[attachment setPermission:@"Edit"];
[attachment setIsFolder:@"True"];

NSError *error;
NSData *attachmentData = [attachment getSerializedDataWithError:&error];
[urlRequest setHTTPBody:attachmentData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```