---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6ea2589847869b8034246e47e8eedb8f2beb2d1e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486403"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const privilegedApproval = {
  userId: "userId-value",
  roleId: "roleId-value",
  approvalType: "approvalType-value",
  approvalState: "approvalState-value",
  approvalDuration: "datetime-value"
};

let res = await client.api('/privilegedApproval')
    .version('beta')
    .post({privilegedApproval : privilegedApproval});

```