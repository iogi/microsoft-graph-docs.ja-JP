---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: fed23eeec26d1d4d3adcd45dbe0f619bcd0f8f27
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513289"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const event = {
  subject: "Let's go for lunch",
  body: {
    contentType: "HTML",
    content: "Does late morning work for you?"
  },
  start: {
      dateTime: "2017-04-15T12:00:00",
      timeZone: "Pacific Standard Time"
  },
  end: {
      dateTime: "2017-04-15T14:00:00",
      timeZone: "Pacific Standard Time"
  },
  location:{
      displayName:"Harry's Bar"
  },
  attendees: [
    {
      emailAddress: {
        address:"samanthab@contoso.onmicrosoft.com",
        name: "Samantha Booth"
      },
      type: "required"
    }
  ]
};

let res = await client.api('/me/events')
    .post({event : event});

```