---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 06f8c4ac11665a9d7e5e03e696d3472e18a83b39
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34482039"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getYammerDeviceUsageUserDetail(period='D7')')
    .version('beta')
    .get();

```