---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 410ee3e8a737a8290a519f05c2d4a78d722c47d3
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34444924"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/worksheets')
    .version('beta')
    .get();

```