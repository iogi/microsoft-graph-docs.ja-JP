---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 26a81cc65ddf0b30fb41fdaea6c63f400898dd95
ms.sourcegitcommit: f50b1feff72182d1e19bfa346304beaf29558b68
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "36461210"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const educationRubric = {
    displayName:"Example Points Rubric",
    description:{
        content:"This is an example of a rubric with points",
        contentType:"text"
    },
    levels:[
        {
            displayName:"Good",
            description:{
                content:"",
                contentType:"text"
            },
            grading:{
                @odata.type:"#microsoft.graph.educationAssignmentPointsGradeType",
                maxPoints:2
            }
        },
        {
            displayName:"Poor",
            description:{
                content:"",
                contentType:"text"
            },
            grading:{
                @odata.type:"#microsoft.graph.educationAssignmentPointsGradeType",
                maxPoints:1
            }
        }
    ],
    qualities:[
        {
            description:{
                content:"Argument",
                contentType:"text"
            },
            criteria:[
                {
                    description:{
                        content:"The essay's argument is persuasive.",
                        contentType:"text"
                    }
                },
                {
                    description:{
                        content:"The essay's argument does not make sense.",
                        contentType:"text"
                    }
                }
            ],
            weight:50.0
        },
        {
            description:{
                content:"Spelling and Grammar",
                contentType:"text"
            },
            criteria:[
                {
                    description:{
                        content:"The essay uses proper spelling and grammar with few or no errors.",
                        contentType:"text"
                    }
                },
                {
                    description:{
                        content:"The essay has numerous errors in spelling and/or grammar.",
                        contentType:"text"
                    }
                }
            ],
            weight:50.0
        }
    ],
    grading:{
        @odata.type:"#microsoft.graph.educationAssignmentPointsGradeType"
    }
};

let res = await client.api('/education/me/rubrics')
    .version('beta')
    .post({educationRubric : educationRubric});

```