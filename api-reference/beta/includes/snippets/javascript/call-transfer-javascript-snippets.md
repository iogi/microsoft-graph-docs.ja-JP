---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 11fc657409b34dec6d4b3e8e7a341270729c3a72
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527141"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const transfer = {
  transferTarget: {
    endpointType: "default",
    identity: {
      user: {
        id: "550fae72-d251-43ec-868c-373732c2704f",
        tenantId: "72f988bf-86f1-41af-91ab-2d7cd011db47",
        displayName: "Heidi Steen"
      }
    },
    languageId: "languageId-value",
    region: "region-value",
    replacesCallId: "replacesCallId-value"
  },
  clientContext: "clientContext-value"
};

let res = await client.api('/app/calls/{id}/transfer')
    .version('beta')
    .post(transfer);

```