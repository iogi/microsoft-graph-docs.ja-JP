---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6f3018c42baf076f064861b43f03d62744be5e9b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496050"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const workbookNamedItem = {
  name: "test7",
  formula: "=SUM(Sheet2!$A$1+Sheet2!$A$2)",
  comment: "Comment for the named item"
};

let res = await client.api('/me/drive/items/{id}/workbook/names/addFormulaLocal')
    .post(workbookNamedItem);

```