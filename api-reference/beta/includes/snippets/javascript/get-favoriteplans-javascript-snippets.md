---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 9599a0c0d7b015e0f6c5c8399b60f0b2ff72a894
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486942"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/planner/favoritePlans')
    .version('beta')
    .get();

```