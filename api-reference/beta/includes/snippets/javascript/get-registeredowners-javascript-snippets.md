---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6e08ebe113c02f5b7b2fda948eb4d8c66e53361d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526776"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/devices/{id}/registeredOwners')
    .version('beta')
    .get();

```