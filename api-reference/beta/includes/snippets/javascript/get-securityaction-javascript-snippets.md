---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e1f58c2ab4589b30baa76c858503dea8a843d354
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485443"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/security/securityActions/{id}')
    .version('beta')
    .get();

```