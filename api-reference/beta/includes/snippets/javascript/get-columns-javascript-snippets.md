---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c5146959d51be22b369ae0ec68b786834f44712e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526166"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns')
    .version('beta')
    .skip(5)
    .top(5)
    .get();

```