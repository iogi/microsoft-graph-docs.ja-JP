---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c1faf2e0ba132dbc2d6c770b7b14fc43320c2bb6
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2019
ms.locfileid: "35859868"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IEducationSchoolCollectionPage schools = graphClient.education().me().schools()
    .buildRequest()
    .get();

```