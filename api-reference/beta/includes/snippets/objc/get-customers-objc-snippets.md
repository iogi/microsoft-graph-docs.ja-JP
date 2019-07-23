---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fac97b31c4c24dfd4079f0254627eb4c2ea9b00c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527334"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/customers"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *bookingCustomerList = [[NSMutableArray alloc] init];
        bookingCustomerList = [jsonFinal valueForKey:@"value"];
        MSGraphBookingCustomer *bookingCustomer = [[MSGraphBookingCustomer alloc] initWithDictionary:[bookingCustomerList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```