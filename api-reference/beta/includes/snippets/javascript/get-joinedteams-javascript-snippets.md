---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fb25f1360fe346df752e93ab70375326fcc7c83d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485024"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/joinedTeams')
    .version('beta')
    .get();

```