---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5d9e2e0685770083f6fa62a9cf9f4ab8d29891a4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496152"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/calendar')
    .delete();

```