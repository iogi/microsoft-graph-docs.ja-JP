---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: add31a19fc8034b12cd2d4b5ac631d775a4346e4
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445792"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/servicePrincipals/{id}/synchronization/jobs/{jobId}/')
    .version('beta')
    .get();

```