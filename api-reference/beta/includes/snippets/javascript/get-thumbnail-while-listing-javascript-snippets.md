---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1f7c280b8ad5e5cf99381e1a2139ef58f2c8d35b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486899"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{item-id}/children')
    .version('beta')
    .expand('thumbnails')
    .get();

```