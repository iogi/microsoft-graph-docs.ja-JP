---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 18ca20629964f013af43a53d655ae9bd05491b78
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503867"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/domains')
    .version('beta')
    .get();

```