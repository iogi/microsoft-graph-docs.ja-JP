---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a68dd0c10d2886dfba47de87a1a191a1da6176fd
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487050"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const privilegedRoleAssignment = {
  userId: "userId-value",
  roleId: "roleId-value"
};

let res = await client.api('/privilegedRoleAssignments')
    .version('beta')
    .post({privilegedRoleAssignment : privilegedRoleAssignment});

```