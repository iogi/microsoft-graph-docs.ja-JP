---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fc3e8b106e3e2cdbee3005dce26af2d97a2df475
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485297"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/alerts')
    .version('beta')
    .get();

```