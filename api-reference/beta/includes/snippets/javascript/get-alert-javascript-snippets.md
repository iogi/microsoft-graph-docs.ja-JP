---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ca58b8a48b41c62ccef997e3c6ac14c32e63db46
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527754"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/alerts/{id}')
    .version('beta')
    .get();

```