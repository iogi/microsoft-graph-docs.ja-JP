---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a567dbf7555c96115fa4aa5b2f5f61bfac47ccff
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527535"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/trustFramework/policies')
    .version('beta')
    .get();

```