---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d5f8ddb3e5c3dadf91625304cbcf6c672b19cbea
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34439046"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/applications/{id}')
    .version('beta')
    .delete();

```