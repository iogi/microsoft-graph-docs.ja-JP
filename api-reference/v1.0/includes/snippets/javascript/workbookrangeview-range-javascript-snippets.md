---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1b30f866aae9d418a7af79c09ce11cd5ecd60e66
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471128"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/range')
    .get();

```