---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d2d254334280a1b4656585873748f3e05d74ab23
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461122"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const educationOutcome = {
    @odata.type:"#microsoft.graph.educationPointsOutcome",
    points:{
        @odata.type:"#microsoft.graph.educationAssignmentPointsGrade",
        points:85.0
    }
};

let res = await client.api('/education/me/assignments/{id}/submissions/{id}/outcomes/{id}')
    .version('beta')
    .update({educationOutcome : educationOutcome});

```