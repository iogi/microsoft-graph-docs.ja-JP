---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 12daaa229d9f88558c1b38dd1797966e5e690696
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464696"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/classes/11014/assignmentCategories/19002')
    .version('beta')
    .delete();

```