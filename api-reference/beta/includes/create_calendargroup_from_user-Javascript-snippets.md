---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d15c102fac82daf75474620b476eabb2c31f65ee
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34457193"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const calendarGroup = {
  name: "name-value",
  classId: "classId-value",
  changeKey: "changeKey-value"
};

let res = await client.api('/me/calendarGroups')
    .version('beta')
    .post({calendarGroup : calendarGroup});

```