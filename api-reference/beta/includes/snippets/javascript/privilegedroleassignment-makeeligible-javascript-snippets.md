---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f54fdda89d556fd0476b14f0a185b836da54f4bb
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503623"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/privilegedRoleAssignments/{id}/makeEligible')
    .version('beta')
    .post();

```