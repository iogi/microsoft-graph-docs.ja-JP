---
description: 自動生成されたファイル。 変更しないでください
ms.openlocfilehash: 845b54100cd26bbf2984bddae5300bcf973307fe
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2019
ms.locfileid: "35889080"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/owners')
    .get();

```