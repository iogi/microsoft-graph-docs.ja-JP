---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 56d8c90693b3b2b1c828d7e381b4ddab079fee9b
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34434379"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const calendar = {
  name: "name-value",
  color: {
  }
};

let res = await client.api('/me/calendarGroups/{id}/calendars')
    .version('beta')
    .post({calendar : calendar});

```