---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d78dd342594f9b7f014c90586de47ef9efcd05c5
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445715"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/servicePrincipals/{id}/synchronization/templates')
    .version('beta')
    .get();

```