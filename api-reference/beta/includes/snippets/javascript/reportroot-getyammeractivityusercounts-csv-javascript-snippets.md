---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5af41740ba2d215ff953d011d8dd3bcab907b4e0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485931"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getYammerActivityUserCounts(period='D7')')
    .version('beta')
    .get();

```