---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ff08acb71ae40c11d2ae987b4dfa5aaa32f9417c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526532"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/root/delta?token=latest')
    .version('beta')
    .get();

```