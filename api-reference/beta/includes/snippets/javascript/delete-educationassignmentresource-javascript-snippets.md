---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c3207cc4709ebc0c17ad8d003ab205c8486df1a8
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35464693"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/education/classes/11021/assignments/19002/resources/22002')
    .version('beta')
    .delete();

```