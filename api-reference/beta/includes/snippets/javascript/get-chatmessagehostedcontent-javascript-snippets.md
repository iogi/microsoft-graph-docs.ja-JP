---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: f09494db874fecd41ab4d7c04e2bf35f52042916
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485232"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/chats/{id}/messages/{id}/hostedContents/{id}')
    .version('beta')
    .get();

```