---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3081ecf1a1e98fb99703fbd3b8521d823fd53b6d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514291"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/contacts/{id}"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphContact *contact = [[MSGraphContact alloc] init];
MSGraphPhysicalAddress *homeAddress = [[MSGraphPhysicalAddress alloc] init];
[homeAddress setStreet:@"123 Some street"];
[homeAddress setCity:@"Seattle"];
[homeAddress setState:@"WA"];
[homeAddress setPostalCode:@"98121"];
[contact setHomeAddress:homeAddress];
[contact setBirthday:@"1974-07-22"];

NSError *error;
NSData *contactData = [contact getSerializedDataWithError:&error];
[urlRequest setHTTPBody:contactData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```