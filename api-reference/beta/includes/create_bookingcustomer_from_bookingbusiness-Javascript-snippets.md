---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3ac4504c7438d00d9c62853d39cb07594c95020f
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34434442"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const bookingCustomer = {
    displayName: "Joni Sherman",
    emailAddress: "jonis@relecloud.com"
};

let res = await client.api('/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/customers')
    .version('beta')
    .post({bookingCustomer : bookingCustomer});

```