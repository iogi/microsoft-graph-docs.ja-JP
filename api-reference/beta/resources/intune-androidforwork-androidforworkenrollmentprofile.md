---
title: androidForWorkEnrollmentProfile リソース タイプ
description: Google のクラウド管理を使用して COSU デバイスを登録するために使われる登録プロファイルです。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: a8300f0daebad439273b8ce414c8df7617fb25c8
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36367058"
---
# <a name="androidforworkenrollmentprofile-resource-type"></a>androidForWorkEnrollmentProfile リソース タイプ

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Google のクラウド管理を使用して COSU デバイスを登録するために使われる登録プロファイルです。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List androidForWorkEnrollmentProfiles](../api/intune-androidforwork-androidforworkenrollmentprofile-list.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) コレクション|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-get.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-create.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|新しい [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) オブジェクトを作成します。|
|[Delete androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-delete.md)|None|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) を削除します。|
|[Update androidForWorkEnrollmentProfile](../api/intune-androidforwork-androidforworkenrollmentprofile-update.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md)|[androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) オブジェクトのプロパティを更新します。|
|[revokeToken action](../api/intune-androidforwork-androidforworkenrollmentprofile-revoketoken.md)|なし|まだ文書化されていません|
|[createToken action](../api/intune-androidforwork-androidforworkenrollmentprofile-createtoken.md)|なし|まだ文書化されていません|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|accountId|String|登録プロファイルが属するテナント GUID。|
|id|文字列|登録プロファイルの一意の GUID。|
|displayName|String|登録プロファイルの表示名。|
|description|String|登録プロファイルの説明。|
|createdDateTime|DateTimeOffset|登録プロファイルが作成された日時。|
|lastModifiedDateTime|DateTimeOffset|登録プロファイルが最後に変更された日時。|
|tokenValue|String|この登録プロファイル用に最後に作成されたトークンの値。|
|tokenExpirationDateTime|DateTimeOffset|最後に作成されたトークンの有効期限が切れる日時。|
|enrolledDeviceCount|Int32|この登録プロファイルを使用して登録した Android デバイスの合計数。|
|qrCodeContent|String|トークン用の QR コードを生成するために使用された文字列。|
|qrCodeImage|[mimeContent](../resources/intune-shared-mimecontent.md)|トークンの QR コードを生成するために使用する文字列。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
  "accountId": "String",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "tokenValue": "String",
  "tokenExpirationDateTime": "String (timestamp)",
  "enrolledDeviceCount": 1024,
  "qrCodeContent": "String",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  }
}
```



