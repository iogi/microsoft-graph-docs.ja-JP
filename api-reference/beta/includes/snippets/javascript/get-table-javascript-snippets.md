---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e6067cf6fbbadc8f15b8bd174f0bbaf320b23be1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527780"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}')
    .version('beta')
    .get();

```