---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c26086b587993a7d446c67582bd2786dea5d170e
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34843704"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const driveItem = {
  parentReference: {
    path: "/drive/root:/Documents"
  },
  name: "Copy of LargeFolder1"
};

let res = await client.api('/me/drive/items/{folder-item-id}/copy')
    .version('beta')
    .post(driveItem);

```