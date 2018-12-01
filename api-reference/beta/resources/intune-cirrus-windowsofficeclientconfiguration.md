---
title: windowsOfficeClientConfiguration リソースの種類
description: Windows 用の office ポリシーの設定について説明するエンティティです。
ms.openlocfilehash: 5e1a3281ec6b970765c81ecfd238026d71066c59
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27068833"
---
# <a name="windowsofficeclientconfiguration-resource-type"></a>windowsOfficeClientConfiguration リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

Windows 用の office ポリシーの設定について説明するエンティティです。

[OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト windowsOfficeClientConfigurations](../api/intune-cirrus-windowsofficeclientconfiguration-list.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)コレクション|[WindowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)オブジェクトのプロパティと関係を一覧表示します。|
|[WindowsOfficeClientConfiguration を取得します。](../api/intune-cirrus-windowsofficeclientconfiguration-get.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)|[WindowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)オブジェクトのプロパティと関係を参照してください。|
|[WindowsOfficeClientConfiguration を作成します。](../api/intune-cirrus-windowsofficeclientconfiguration-create.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)|新しい[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)オブジェクトを作成します。|
|[WindowsOfficeClientConfiguration を削除します。](../api/intune-cirrus-windowsofficeclientconfiguration-delete.md)|なし|の[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)を削除します。|
|[WindowsOfficeClientConfiguration を更新します。](../api/intune-cirrus-windowsofficeclientconfiguration-update.md)|[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)|[WindowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|Office クライアントの構成のポリシーの id。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|userPreferencePayload|Stream|JSON の環境設定は、バイナリ形式の文字列は、ユーザーがこれらの値をオーバーライドすることができます。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|policyPayload|Stream|JSON のポリシー設定はバイナリ形式の文字列は、ユーザーがこれらの値を変更することはできません。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|説明|String|管理者には、office クライアントの説明の構成のポリシーが用意されています。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|displayName|String|管理者は、office クライアントの構成のポリシーの名前を提供します。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|priority|Int32|優先度の値がテナントの下にある各ポリシーの一意の値にする必要があり、競合の解決に使用する、値が低い優先順位が高いことを意味します。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|lastModifiedDateTime|DateTime|ポリシーの最終変更された日付時刻スタンプ。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|userCheckinSummary|[officeUserCheckinSummary](../resources/intune-cirrus-officeusercheckinsummary.md)|ポリシーの概要チェックのユーザーです。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|checkinStatuses|[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)コレクション|Office クライアントでは、チェック状態の一覧です。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|assignments|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)コレクション|一連のポリシーの割り当てをグループ化します。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsOfficeClientConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsOfficeClientConfiguration",
  "id": "String (identifier)",
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "String",
  "displayName": "String",
  "priority": 1024,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 1024,
    "failedUserCount": 1024
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "String",
      "deviceName": "String",
      "devicePlatform": "String",
      "devicePlatformVersion": "String",
      "wasSuccessful": true,
      "userId": "String",
      "checkinDateTime": "String (timestamp)",
      "errorMessage": "String",
      "appliedPolicies": [
        "String"
      ]
    }
  ]
}
```


