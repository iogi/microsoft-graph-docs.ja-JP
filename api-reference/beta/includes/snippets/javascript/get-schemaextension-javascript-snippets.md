---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1a67d671b5ee87c33528fa1e42e82ef8788a1519
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527861"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/schemaExtensions/graphlearn_test')
    .version('beta')
    .get();

```