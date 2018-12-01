---
title: managedAppRegistration リソース タイプ
description: ManagedAppEntity は、アプリ管理ワークフロー下にある他のすべてのエンティティ タイプの基本型です。
ms.openlocfilehash: bf05e7180f27be9c813f8fbb05346893fa6db172
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27069449"
---
# <a name="managedappregistration-resource-type"></a>managedAppRegistration リソース タイプ

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

ManagedAppEntity は、アプリ管理ワークフロー下にある他のすべてのエンティティ タイプの基本型です。
ManagedAppRegistration リソースは、組織のメンバーに使用されるアプリの詳細を管理機能と共に示します。
## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List managedAppRegistrations](../api/intune-mam-managedappregistration-list.md)|[managedAppRegistration](../resources/intune-mam-managedappregistration.md) コレクション|[managedAppRegistration](../resources/intune-mam-managedappregistration.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get managedAppRegistration](../api/intune-mam-managedappregistration-get.md)|[managedAppRegistration](../resources/intune-mam-managedappregistration.md)|[managedAppRegistration](../resources/intune-mam-managedappregistration.md) オブジェクトのプロパティとリレーションを読み取ります。|
|[getUserIdsWithFlaggedAppRegistration function](../api/intune-mam-managedappregistration-getuseridswithflaggedappregistration.md)|String コレクション|まだ文書化されていません|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|作成日時|
|lastSyncDateTime|DateTimeOffset|アプリが管理サービスと最後に同期した日付と時刻。|
|applicationVersion|String|アプリのバージョン|
|managementSdkVersion|String|アプリ管理の SDK バージョン|
|platformVersion|String|オペレーティング システムのバージョン|
|deviceType|String|ホスト デバイスの種類|
|deviceTag|String|アプリ管理 SDK が生成したタグ。同じデバイスでホストされているアプリの関連付けに役立ちます。 あらゆる状況でのアプリの関連付けを保証するものではありません。|
|deviceName|String|ホスト デバイスの名前|
|managedDeviceId|String|ホスト ・ デバイスの管理デバイスの識別子です。 ホスト ・ デバイスが管理されている場合にも、値を空にする可能性があります。|
|azureADDeviceId|String|ホスト ・ デバイスの Azure Active Directory のデバイスの識別子です。 ホスト ・ デバイスは、Azure Active Directory が登録されている場合でも、値を空にする可能性があります。|
|deviceModel|String|現在のアプリケーションの登録用のデバイス モデル |
|deviceManufacturer|String|現在のアプリケーションの登録のためのデバイスの製造元 |
|flaggedReasons|[managedAppFlaggedReason](../resources/intune-mam-managedappflaggedreason.md)コレクション|アプリ登録にフラグが設定された、0 個以上の理由。 例: ルートのデバイスで実行されているアプリ|
|userId|String|このアプリの登録が属するユーザー ID。|
|appIdentifier|[mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)|アプリ パッケージの識別子|
|id|String|エンティティのキー。|
|version|String|エンティティのバージョン。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|appliedPolicies|[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) コレクション|登録済みのアプリが管理サービスと最後に同期したときに、既に適用されていた 0 個以上のポリシーです。|
|intendedPolicies|[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) コレクション|現時点で、管理者がアプリに対して意図した 0 個以上のポリシーです。|
|operations|[managedAppOperation](../resources/intune-mam-managedappoperation.md) コレクション|アプリ登録でトリガーされた、0 個以上の長時間実行の操作です。|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppRegistration",
  "createdDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "applicationVersion": "String",
  "managementSdkVersion": "String",
  "platformVersion": "String",
  "deviceType": "String",
  "deviceTag": "String",
  "deviceName": "String",
  "managedDeviceId": "String",
  "azureADDeviceId": "String",
  "deviceModel": "String",
  "deviceManufacturer": "String",
  "flaggedReasons": [
    "String"
  ],
  "userId": "String",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "String (identifier)",
  "version": "String"
}
```




