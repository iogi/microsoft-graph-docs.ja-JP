---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 663077ea71383a76e28c0ad8c14baa253b408282
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514166"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/entireColumn')
    .get();

```