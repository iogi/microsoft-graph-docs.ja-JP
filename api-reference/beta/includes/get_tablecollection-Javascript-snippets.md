---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f7c8e6748e86998b8ffc7c5cb21b3db22fa0b896
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445659"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/tables')
    .version('beta')
    .get();

```