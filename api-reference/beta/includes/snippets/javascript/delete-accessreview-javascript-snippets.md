---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 687bbe11a3fa234f21e406fc709e3694d55cf912
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485064"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/accessReviews/2975E9B5-44CE-4E71-93D3-30F03B5AA992/')
    .version('beta')
    .delete();

```