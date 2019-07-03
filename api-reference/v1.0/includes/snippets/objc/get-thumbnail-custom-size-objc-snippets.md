---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 499cbb962dffedf6abea9a6c881b7d4511dfe144
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513785"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{item-id}/thumbnails?select=c300x400_Crop"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *thumbnailSetList = [[NSMutableArray alloc] init];
        thumbnailSetList = [jsonFinal valueForKey:@"value"];
        MSGraphThumbnailSet *thumbnailSet = [[MSGraphThumbnailSet alloc] initWithDictionary:[thumbnailSetList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```