---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5a8af9420f8cb6d8c6eba2e251ea52fa98f80b00
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34438961"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/events/{id}/attachments/{id}')
    .version('beta')
    .delete();

```