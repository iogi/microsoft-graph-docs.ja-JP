---
title: dataSharingConsent リソースの種類
description: データの共有についてを同意するものとします。
ms.openlocfilehash: 152b367161dc9a734a20e007ac1b2c0d02d0c99f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27074254"
---
# <a name="datasharingconsent-resource-type"></a>dataSharingConsent リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

データの共有についてを同意するものとします。
## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト dataSharingConsents](../api/intune-devices-datasharingconsent-list.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)コレクション|[DataSharingConsent](../resources/intune-devices-datasharingconsent.md)オブジェクトのプロパティと関係を一覧表示します。|
|[DataSharingConsent を取得します。](../api/intune-devices-datasharingconsent-get.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|[DataSharingConsent](../resources/intune-devices-datasharingconsent.md)オブジェクトのプロパティと関係を参照してください。|
|[DataSharingConsent を作成します。](../api/intune-devices-datasharingconsent-create.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|新しい[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)オブジェクトを作成します。|
|[DataSharingConsent を削除します。](../api/intune-devices-datasharingconsent-delete.md)|なし|の[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)を削除します。|
|[DataSharingConsent を更新します。](../api/intune-devices-datasharingconsent-update.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|[DataSharingConsent](../resources/intune-devices-datasharingconsent.md)オブジェクトのプロパティを更新します。|
|[consentToDataSharing アクション](../api/intune-devices-datasharingconsent-consenttodatasharing.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|まだ文書化されていません|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|データ共有同意 Id|
|serviceDisplayName|String|サービス作業の流れの表示名|
|termsUrl|String|同意の共有データの TermsUrl|
|付与|ブール値|同意の共有データに付与されている状態|
|grantDateTime|DateTimeOffset|同意は、このアカウントに与えられました。|
|grantedByUpn|String|このアカウントに許可を付与するユーザーの Upn|
|grantedByUserId|String|このアカウントに許可を付与するユーザーのユーザー Id|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.dataSharingConsent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.dataSharingConsent",
  "id": "String (identifier)",
  "serviceDisplayName": "String",
  "termsUrl": "String",
  "granted": true,
  "grantDateTime": "String (timestamp)",
  "grantedByUpn": "String",
  "grantedByUserId": "String"
}
```




