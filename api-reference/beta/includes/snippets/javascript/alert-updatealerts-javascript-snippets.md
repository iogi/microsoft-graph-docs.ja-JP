---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 45a1c143054dae06e329730f1867c020bb71af56
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526366"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const alert = {
  value: [
    {
      assignedTo: "String",
      closedDateTime: "String (timestamp)",
      comments: ["String"],
      feedback: {@odata.type: "microsoft.graph.alertFeedback"},
      id: "String (identifier)",
      status: {@odata.type: "microsoft.graph.alertStatus"},
      tags: ["String"],
      vendorInformation:
        {
          provider: "String",
          vendor: "String"
        }
    }
  ]
};

let res = await client.api('/security/alerts/updateAlerts')
    .version('beta')
    .post(alert);

```