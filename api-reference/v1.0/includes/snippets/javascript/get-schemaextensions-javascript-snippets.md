---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a3e639af0aee8cf1ce5fc456b52b29600e87d18c
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471967"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/schemaExtensions')
    .filter('id eq 'graphlearn_test'')
    .get();

```