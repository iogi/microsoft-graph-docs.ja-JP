---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5244ae5193c1717f9798b86f548ef109661c402d
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34441382"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getOffice365GroupsActivityGroupCounts(period='D7')')
    .version('beta')
    .get();

```