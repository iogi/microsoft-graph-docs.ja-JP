---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a42073e11996ab43184790494ec4d37048f3fe2e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485949"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/domains/contoso.com/serviceConfigurationRecords"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *domainDnsRecordList = [[NSMutableArray alloc] init];
        domainDnsRecordList = [jsonFinal valueForKey:@"value"];
        MSGraphDomainDnsRecord *domainDnsRecord = [[MSGraphDomainDnsRecord alloc] initWithDictionary:[domainDnsRecordList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```