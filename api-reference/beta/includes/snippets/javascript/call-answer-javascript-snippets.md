---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2079cd1d22cef1632c0d008ca858229c4ae43f22
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526353"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const answer = {
  callbackUri: "callbackUri-value",
  mediaConfig: {
    @odata.type: "#microsoft.graph.appHostedMediaConfig",
    blob: "<media config blob>"
  },
  acceptedModalities: [
    "audio"
  ]
};

let res = await client.api('/app/calls/{id}/answer')
    .version('beta')
    .post(answer);

```