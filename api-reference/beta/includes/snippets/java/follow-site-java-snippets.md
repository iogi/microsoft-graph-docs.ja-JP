---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 93a39a4a918e4af25f01841c86d6ea2b73f42bdd
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2019
ms.locfileid: "35869706"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Site> valueList = new LinkedList<Site>();
Site value = new Site();
value.id = "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740";

valueList.add(value);
Site value1 = new Site();
value1.id = "contoso.sharepoint.com,da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851";

valueList.add(value1);

graphClient.users("{user-id}").followedSites()
    .add(valueList)
    .buildRequest()
    .post();

```