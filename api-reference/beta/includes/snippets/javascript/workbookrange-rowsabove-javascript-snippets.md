---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 15603d9b0b9926480d4d54f7977ec0de2814e529
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504068"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/drive/root/workbook/worksheets/{id}/range/rowsAbove(count=2)')
    .version('beta')
    .post();

```