---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 16325749053d48b544e3e4ebdfbfd3627d332b89
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34440255"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const message = {
    subject:"Did you see last night's game?",
    importance:"Low",
    body:{
        contentType:"HTML",
        content:"They were <b>awesome</b>!"
    },
    toRecipients:[
        {
            emailAddress:{
                address:"AdeleV@contoso.onmicrosoft.com"
            }
        }
    ]
};

let res = await client.api('/me/messages')
    .version('beta')
    .post({message : message});

```