---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 472b6d69d00c685e621295cb0ff43a6b05372779
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527315"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const contactFolder = {
  parentFolderId: "parentFolderId-value",
  displayName: "displayName-value"
};

let res = await client.api('/me/contactFolders')
    .version('beta')
    .post({contactFolder : contactFolder});

```