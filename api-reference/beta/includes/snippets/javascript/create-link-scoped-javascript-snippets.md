---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 61393570191320e984864693f2bfe29a820c5cda
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486453"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const permission = {
  type: "edit",
  scope: "organization"
};

let res = await client.api('/me/drive/items/{item-id}/createLink')
    .version('beta')
    .post(permission);

```