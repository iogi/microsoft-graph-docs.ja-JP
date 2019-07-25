---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 41f7c5a26fd800d4efbc62ccb43dde2f713c87d3
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2019
ms.locfileid: "35885219"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

MailboxSettings mailboxSettings = new MailboxSettings();
mailboxSettings.additionalDataManager().put("@odata.context", new JsonPrimitive("https://graph.microsoft.com/v1.0/$metadata#Me/mailboxSettings"));
AutomaticRepliesSetting automaticRepliesSetting = new AutomaticRepliesSetting();
automaticRepliesSetting.status = AutomaticRepliesStatus.SCHEDULED;
DateTimeTimeZone scheduledStartDateTime = new DateTimeTimeZone();
scheduledStartDateTime.dateTime = "2016-03-20T18:00:00";
scheduledStartDateTime.timeZone = "UTC";
automaticRepliesSetting.scheduledStartDateTime = scheduledStartDateTime;
DateTimeTimeZone scheduledEndDateTime = new DateTimeTimeZone();
scheduledEndDateTime.dateTime = "2016-03-28T18:00:00";
scheduledEndDateTime.timeZone = "UTC";
automaticRepliesSetting.scheduledEndDateTime = scheduledEndDateTime;
mailboxSettings.automaticRepliesSetting = automaticRepliesSetting;

graphClient.customRequest("/me/mailboxSettings", MailboxSettings.class)
    .buildRequest()
    .patch(mailboxSettings);

```