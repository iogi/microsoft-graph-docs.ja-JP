---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 438730c3efb2fc172c2fa31d7f92a7dc0ffae261
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34446121"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/servicePrincipals')
    .version('beta')
    .get();

```