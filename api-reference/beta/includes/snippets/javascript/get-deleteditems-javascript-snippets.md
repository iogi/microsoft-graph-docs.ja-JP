---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: aed27b815116d4f792bc4f7b7e46f9fec7c729be
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526535"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/directory/deleteditems/microsoft.graph.group')
    .version('beta')
    .get();

```