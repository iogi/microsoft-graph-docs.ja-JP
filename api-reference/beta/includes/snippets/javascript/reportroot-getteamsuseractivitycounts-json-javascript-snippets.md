---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 44c752f47a707484314f3cfa8b4a546dd6ffdc34
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486714"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/reports/getTeamsUserActivityCounts(period='D7')')
    .version('beta')
    .get();

```