---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6ed304b1ccb866413b1b9abe953116bdb65d2810
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504573"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/following/{item-id}')
    .version('beta')
    .delete();

```