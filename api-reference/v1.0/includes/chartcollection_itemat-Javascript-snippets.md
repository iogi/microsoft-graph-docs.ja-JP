---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e446cb60c899b4eaa71d5dd4eda683b54404e7a1
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34434760"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookChart = {
  index: 8
};

let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/itemAt')
    .post({workbookChart : workbookChart});

```