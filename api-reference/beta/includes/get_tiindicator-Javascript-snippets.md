---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 270ca5f19e246778d47c0287a69e746ccc7ab269
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445351"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/tiIndicators/{id}')
    .version('beta')
    .get();

```