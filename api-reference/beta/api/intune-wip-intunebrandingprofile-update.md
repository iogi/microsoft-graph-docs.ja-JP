---
title: IntuneBrandingProfile の更新
description: IntuneBrandingProfile オブジェクトのプロパティを更新します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 3b82968b2b0efc16238fe84da61253fcf594ca8a
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36350189"
---
# <a name="update-intunebrandingprofile"></a>IntuneBrandingProfile の更新

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

[IntuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)オブジェクトのプロパティを更新します。

## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementApps.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|DeviceManagementApps.ReadWrite.All|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、 [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)オブジェクトの JSON 表記を指定します。

次の表に、 [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|プロファイルキー|
|profileName|String|プロファイルの名前|
|profileDescription|String|プロファイルの説明|
|isDefaultProfile|Boolean|プロファイルが既定として使用されるかどうかを表すブール値|
|createdDateTime|DateTimeOffset|BrandingProfile が作成された時刻|
|lastModifiedDateTime|DateTimeOffset|BrandingProfile が最後に変更された時刻|
|displayName|String|エンドユーザーに表示される会社名または組織名|
|contactITName|String|IT サポートを担当する個人または組織の名前|
|contactITPhoneNumber|String|IT サポートを担当する個人または組織の電話番号|
|contactITEmailAddress|String|IT サポートを担当する個人または組織の電子メールアドレス|
|contactITNotes|String|IT サポートを担当する個人または組織に関するテキストコメント|
|privacyUrl|String|会社/組織のプライバシーポリシーの URL|
|onlineSupportSiteUrl|String|会社または組織の IT ヘルプデスクサイトへの URL|
|onlineSupportSiteName|String|会社/組織の IT ヘルプデスクサイトの表示名|
|themeColor|[rgbColor](../resources/intune-shared-rgbcolor.md)|会社のポータルアプリケーションと web ポータルで使用される主要なテーマの色|
|showLogo|Boolean|管理者が指定したロゴ画像が表示されるかどうかを表すブール値|
|showDisplayNameNextToLogo|Boolean|管理者が指定した表示名がロゴ画像の隣に表示されるかどうかを表すブール値|
|themeColorLogo|[mimeContent](../resources/intune-shared-mimecontent.md)|ロゴの背景色がテーマになっている、ポータルサイトアプリに表示されるロゴ画像|
|lightBackgroundLogo|[mimeContent](../resources/intune-shared-mimecontent.md)|ロゴの背景が明るい、ポータルサイトアプリに表示されるロゴ画像|
|landingPageCustomizedImage|[mimeContent](../resources/intune-shared-mimecontent.md)|会社のポータルアプリのランディングページに表示されるカスタマイズ画像|
|customPrivacyMessage|String|デバイスで管理者がアクセスできる内容に関するテキストコメント|
|isRemoveDeviceDisabled|Boolean|Adminsistrator が企業所有のデバイスで [デバイスの削除] アクションを無効にしているかどうかを表すブール値。|
|isFactoryResetDisabled|Boolean|Adminsistrator が企業所有のデバイスで "出荷時のリセット" アクションを無効にしているかどうかを表すブール値。|



## <a name="response"></a>応答
成功した場合、このメソッド`200 OK`は応答コードと、応答本文で更新された[intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md)オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}
Content-type: application/json
Content-length: 1334

{
  "@odata.type": "#microsoft.graph.intuneBrandingProfile",
  "profileName": "Profile Name value",
  "profileDescription": "Profile Description value",
  "isDefaultProfile": true,
  "displayName": "Display Name value",
  "contactITName": "Contact ITName value",
  "contactITPhoneNumber": "Contact ITPhone Number value",
  "contactITEmailAddress": "Contact ITEmail Address value",
  "contactITNotes": "Contact ITNotes value",
  "privacyUrl": "https://example.com/privacyUrl/",
  "onlineSupportSiteUrl": "https://example.com/onlineSupportSiteUrl/",
  "onlineSupportSiteName": "Online Support Site Name value",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1,
    "g": 1,
    "b": 1
  },
  "showLogo": true,
  "showDisplayNameNextToLogo": true,
  "themeColorLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "customPrivacyMessage": "Custom Privacy Message value",
  "isRemoveDeviceDisabled": true,
  "isFactoryResetDisabled": true
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1506

{
  "@odata.type": "#microsoft.graph.intuneBrandingProfile",
  "id": "fcd6136c-136c-fcd6-6c13-d6fc6c13d6fc",
  "profileName": "Profile Name value",
  "profileDescription": "Profile Description value",
  "isDefaultProfile": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "contactITName": "Contact ITName value",
  "contactITPhoneNumber": "Contact ITPhone Number value",
  "contactITEmailAddress": "Contact ITEmail Address value",
  "contactITNotes": "Contact ITNotes value",
  "privacyUrl": "https://example.com/privacyUrl/",
  "onlineSupportSiteUrl": "https://example.com/onlineSupportSiteUrl/",
  "onlineSupportSiteName": "Online Support Site Name value",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1,
    "g": 1,
    "b": 1
  },
  "showLogo": true,
  "showDisplayNameNextToLogo": true,
  "themeColorLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "customPrivacyMessage": "Custom Privacy Message value",
  "isRemoveDeviceDisabled": true,
  "isFactoryResetDisabled": true
}
```






