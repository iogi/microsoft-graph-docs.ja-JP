---
title: complianceState 列挙型
description: コンプライアンスの状態です。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: enumPageType
ms.openlocfilehash: 18149f0493f1591c59e5bef98dc9a36f148a600c
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36319210"
---
# <a name="compliancestate-enum-type"></a>complianceState 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

コンプライアンスの状態です。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|不明|.0|わかり.|
|要件|1-d|要件.|
|互換性|pbm-2|デバイスは非準拠で、企業リソースからブロックされます。|
|異なる|1/3|他のルールと競合しています。|
|error|2/4|Error。|
|inGracePeriod|254|デバイスは準拠していないが、会社のリソースにアクセスできる|
|configManager|255|構成マネージャーによる管理|



