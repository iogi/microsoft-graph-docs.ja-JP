---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 473f175b29fa98155247e85d65d157b808a8442c
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2019
ms.locfileid: "35879057"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/onenote/notebooks/{id}/sectionGroups')
    .version('beta')
    .get();

```