---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 86add7d946d8f1d5614d3a246ef39e82fb924cf4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526546"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/conversations')
    .version('beta')
    .get();

```