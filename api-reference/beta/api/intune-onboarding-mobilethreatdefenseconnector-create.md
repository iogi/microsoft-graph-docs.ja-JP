---
title: Create mobileThreatDefenseConnector
description: 新しい mobileThreatDefenseConnector オブジェクトを作成します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 6653d9eb4abc5705eaa8a2dff61c0a758e9a05cf
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36352582"
---
# <a name="create-mobilethreatdefenseconnector"></a>Create mobileThreatDefenseConnector

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

新しい [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) オブジェクトを作成します。

## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementServiceConfig.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|DeviceManagementServiceConfig.ReadWrite.All|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/mobileThreatDefenseConnectors
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、mobileThreatDefenseConnector オブジェクトの JSON 表記を指定します。

次の表に、mobileThreatDefenseConnector 作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|まだ文書化されていません|
|lastHeartbeatDateTime|DateTimeOffset|データ同期パートナーから受信した最後のハートビートの日時|
|partnerState|[mobileThreatPartnerTenantState](../resources/intune-onboarding-mobilethreatpartnertenantstate.md)|このアカウントのデータ同期パートナーの状態。 使用可能な値は、`unavailable`、`available`、`enabled`、`unresponsive` です。|
|androidEnabled|Boolean|Android において、準拠評価時にデータ同期パートナーからのデータを使用するかどうかを設定します|
|iosEnabled|Boolean|IOS において、準拠評価時にデータ同期パートナーからのデータを使用するかどうかを取得または設定します|
|windowsEnabled|Boolean|Windows の場合は、コンプライアンスの評価時にデータ同期パートナーからのデータを使用するかどうかを取得または設定します。|
|macEnabled|Boolean|Mac の場合は、コンプライアンス評価中にデータ同期パートナーからのデータを使用する必要があるかどうかを取得または設定します。|
|androidDeviceBlockedOnMissingPartnerData|Boolean|Android において、デバイスを準拠させる前に Intune がデータ同期パートナーからデータを受信する必要があるかどうかを設定します|
|iosDeviceBlockedOnMissingPartnerData|Boolean|IOS において、デバイスを準拠させる前に Intune がデータ同期パートナーからデータを受信する必要があるかどうかを設定します|
|windowsDeviceBlockedOnMissingPartnerData|Boolean|Windows の場合は、デバイスに準拠したマークを付ける前に、Intune がデータ同期パートナーからデータを受信する必要があるかどうかを設定します。|
|macDeviceBlockedOnMissingPartnerData|Boolean|Mac の場合、デバイスに準拠させる前に Intune がデータ同期パートナーからデータを受信する必要があるかどうかを取得または設定します。|
|partnerUnsupportedOsVersionBlocked|ブール型|データ同期パートナーの最小バージョンの要件を満たさない、有効なプラットフォーム上のデバイスをブロックするかどうかを取得または設定します|
|partnerUnresponsivenessThresholdInDays|Int32|このパートナー統合に関する、テナントごとの無応答許容範囲を取得または設定します|
|allowPartnerToCollectIOSApplicationMetadata|Boolean|IOS デバイスでは、管理者が、インストールされたアプリケーションに関するメタデータを Intune からも収集できるかどうかを管理者が構成できるようにします。|



## <a name="response"></a>応答
成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/beta/deviceManagement/mobileThreatDefenseConnectors
Content-type: application/json
Content-length: 622

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "windowsEnabled": true,
  "macEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "windowsDeviceBlockedOnMissingPartnerData": true,
  "macDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6,
  "allowPartnerToCollectIOSApplicationMetadata": true
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 671

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "e4bede14-de14-e4be-14de-bee414debee4",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "windowsEnabled": true,
  "macEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "windowsDeviceBlockedOnMissingPartnerData": true,
  "macDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6,
  "allowPartnerToCollectIOSApplicationMetadata": true
}
```






