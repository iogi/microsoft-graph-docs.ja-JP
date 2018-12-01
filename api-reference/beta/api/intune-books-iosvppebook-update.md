---
title: iosVppEBook の更新
description: iosVppEBook オブジェクトのプロパティを更新します。
ms.openlocfilehash: c0b0b067eea640fe47367e7cbe1ff897e0ac8ef3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27066658"
---
# <a name="update-iosvppebook"></a>iosVppEBook の更新

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

[iosVppEBook](../resources/intune-books-iosvppebook.md) オブジェクトのプロパティを更新します。
## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementApps.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必須。|
|Accept|application/json|

## <a name="request-body"></a>要求本文
要求本文で、[iosVppEBook](../resources/intune-books-iosvppebook.md) オブジェクトの JSON 表記を指定します。

次の表に、[iosVppEBook](../resources/intune-books-iosvppebook.md) の作成時に必要になるプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティのキー。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|displayName|String|電子ブックの名前。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|説明|String|説明。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|publisher|String|発行元です。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|publishedDateTime|DateTimeOffset|電子ブックが発行された日時。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|largeCover|[mimeContent](../resources/intune-shared-mimecontent.md)|ブック カバー。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|createdDateTime|DateTimeOffset|電子ブック ファイルが作成された日時。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|電子ブックが最後に変更された日時。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|informationUrl|String|詳細情報の URL。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|privacyInformationUrl|String|プライバシーに関する声明の URL。 [managedEBook](../resources/intune-books-managedebook.md) から継承します|
|vppTokenId|Guid|Vpp トークン ID。|
|appleId|String|Vpp トークンに関連付けられている Apple ID。|
|vppOrganizationName|String|Vpp トークンの組織の名前。|
|genres|String コレクション|ジャンル。|
|language|String|言語。|
|seller|String|販売元。|
|totalLicenseCount|Int32|ライセンスの合計数。|
|usedLicenseCount|Int32|使用されているライセンスの数。|



## <a name="response"></a>応答
成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [iosVppEBook](../resources/intune-books-iosvppebook.md) オブジェクトを返します。

## <a name="example"></a>例
### <a name="request"></a>要求
以下は、要求の例です。
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}
Content-type: application/json
Content-length: 806

{
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 964

{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "id": "3b9f627e-627e-3b9f-7e62-9f3b7e629f3b",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```




