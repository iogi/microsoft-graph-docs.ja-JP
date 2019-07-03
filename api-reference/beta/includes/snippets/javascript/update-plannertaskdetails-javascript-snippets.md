---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 96a533306dbab6131cf60ea1167073c1a7ffbaf1
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504005"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const plannerTaskDetails = {
  previewType: "noPreview",
  references: {
    http%3A//developer%2Emicrosoft%2Ecom:{
      @odata.type: "microsoft.graph.plannerExternalReference",
      alias: "Documentation",
      previewPriority: " !",
      type: "Other"
    },
    https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer:{
      @odata.type: "microsoft.graph.plannerExternalReference",
      previewPriority: "  !!",
    },
    http%3A//www%2Ebing%2Ecom: null
  },
  checklist: {
    95e27074-6c4a-447a-aa24-9d718a0b86fa:{
      @odata.type: "microsoft.graph.plannerChecklistItem",
      title: "Update task details",
      isChecked: true
    },
    d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff:{
      @odata.type: "microsoft.graph.plannerChecklistItem",
      isChecked: true,
    },
    a93c93c5-10a6-4167-9551-8bafa09967a7: null
  }
};

let res = await client.api('/planner/tasks/gcrYAaAkgU2EQUvpkNNXLGQAGTtu/details')
    .version('beta')
    .update({plannerTaskDetails : plannerTaskDetails});

```