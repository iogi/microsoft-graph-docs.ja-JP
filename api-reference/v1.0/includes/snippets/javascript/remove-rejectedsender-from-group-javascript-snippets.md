---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ce772a8d1cdd1654de0175e8b330fafc35ac3abc
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514343"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/rejectedSenders/$ref')
    .delete();

```