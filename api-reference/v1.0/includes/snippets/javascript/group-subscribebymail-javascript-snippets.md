---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 0b29eb1ac9c1b85785e96725b0bc7e175e6f8337
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496097"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/{id}/subscribeByMail')
    .post();

```