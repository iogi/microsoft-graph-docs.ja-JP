---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fe35af2150fb7ff78d0c7672d109c736bf09139e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526668"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/tables/{id|name}/rows?$top=5&$skip=5"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *workbookTableRowList = [[NSMutableArray alloc] init];
        workbookTableRowList = [jsonFinal valueForKey:@"value"];
        MSGraphWorkbookTableRow *workbookTableRow = [[MSGraphWorkbookTableRow alloc] initWithDictionary:[workbookTableRowList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```