---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 35732ba3864b75624d169cb1e14fc2a639031e0c
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445883"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/subscriptions/{id}')
    .version('beta')
    .get();

```