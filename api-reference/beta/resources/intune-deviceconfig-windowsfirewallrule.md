---
title: windowsFirewallRule リソースの種類
description: Windows ファイアウォールを介したトラフィックを制御するルール。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 4e07a78db6d30ed6256f5491c57c0de7e3af0946
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36371118"
---
# <a name="windowsfirewallrule-resource-type"></a>windowsFirewallRule リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Windows ファイアウォールを介したトラフィックを制御するルール。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|displayName|String|ルールの表示名。 一意である必要はありません。|
|description|String|ルールの説明。|
|パッケージ Efamilyname|String|ファイアウォールルールの影響を受ける Microsoft Store アプリケーションのパッケージファミリー名。|
|パス|String|ファイアウォールルールの影響を受けるアプリの完全なファイルパス。|
|serviceName|String|アプリケーションではなく、サービスがトラフィックを送受信している場合に使用される名前。|
|プロトコール|Int32|0-255 IP プロトコルを表す番号 (TCP = 6、UDP = 17)。 指定しない場合、既定値は All です。 有効な値は 0 ~ 255|
|localPortRanges|文字列コレクション|ローカルポート範囲のリスト。 たとえば、"100-120"、"200"、"300-320" などです。 指定しない場合、既定値は All です。|
|remotePortRanges|文字列コレクション|リモートポート範囲の一覧。 たとえば、"100-120"、"200"、"300-320" などです。 指定しない場合、既定値は All です。|
|localAddressRanges|文字列コレクション|ルールでカバーされているローカルアドレスのリスト。 既定は任意のアドレスです。 有効なトークンは次のとおりです。<ul><li>"*" はローカルアドレスを示します。 指定する場合は、このトークンのみが含まれている必要があります。</li><li>サブネットは、サブネットマスクまたはネットワークプレフィックス表記のどちらかを使用して指定できます。 サブネットマスクもネットワークプレフィックスも指定されていない場合、サブネットマスクは既定で255.255.255.255 になります。</li><li>有効な IPv6 アドレス。</li><li>スペースを含まない「開始アドレスと終了アドレス」の形式の IPv4 アドレス範囲。</li><li>「開始アドレス-終了アドレス」の形式の IPv6 アドレス範囲。スペースは含まれません。</li></ul>|
|remoteAddressRanges|文字列コレクション|ルールの対象となるリモートアドレスを指定するトークンの一覧です。 トークンの大文字と小文字は区別されません。 既定は任意のアドレスです。 有効なトークンは次のとおりです。<ul><li>"*" は任意のリモートアドレスを示します。 指定する場合は、このトークンのみが含まれている必要があります。</li><li>"Defaultgateway"</li><li>DHCP</li><li>DSN</li><li>獲得</li><li>"Intranet" (Windows バージョンでサポートされている 1809 +)</li><li>"RmtIntranet" (Windows バージョンでサポートされている 1809 +)</li><li>"Internet" (Windows バージョンでサポートされている 1809 +)</li><li>"Ply2Renders" (Windows バージョン1809以降でサポートされています)</li><li>"LocalSubnet" は、ローカルサブネット上のローカルアドレスを示します。</li><li>サブネットは、サブネットマスクまたはネットワークプレフィックス表記のどちらかを使用して指定できます。 サブネットマスクもネットワークプレフィックスも指定されていない場合、サブネットマスクは既定で255.255.255.255 になります。</li><li>有効な IPv6 アドレス。</li><li>スペースを含まない「開始アドレスと終了アドレス」の形式の IPv4 アドレス範囲。</li><li>「開始アドレス-終了アドレス」の形式の IPv6 アドレス範囲。スペースは含まれません。</li></ul>|
|profileTypes|[windowsFirewallRuleNetworkProfileTypes](../resources/intune-deviceconfig-windowsfirewallrulenetworkprofiletypes.md)|ルールが属するプロファイルを指定します。 指定しない場合、既定値は All です。 使用可能な値は、`notConfigured`、`domain`、`private`、`public` です。|
|action|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|ルールによって適用されるアクション。 指定しない場合、既定値を使用できます。 可能な値は、`notConfigured`、`blocked`、`allowed` です。|
|trafficDirection|[windowsFirewallRuleTrafficDirectionType](../resources/intune-deviceconfig-windowsfirewallruletrafficdirectiontype.md)|ルールが有効になっているトラフィックの方向。 指定しない場合、既定値は "Out" です。可能な値は`notConfigured`、 `out`、 `in`、です。|
|interfaceTypes|[windowsFirewallRuleInterfaceTypes](../resources/intune-deviceconfig-windowsfirewallruleinterfacetypes.md)|ルールのインターフェイスの種類。 使用可能な値は、`notConfigured`、`remoteAccess`、`wireless`、`lan` です。|
|edgeTraversal|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|このルールに対してエッジトラバーサルを有効にするか無効にするかを示します。 EdgeTraversal の設定は、特定の受信トラフィックで、Teredo トンネリングテクノロジを使用して Nat およびその他のエッジデバイスをトンネリングできることを示します。 この設定を正しく動作させるには、受信ファイアウォールルールを持つアプリケーションまたはサービスが IPv6 をサポートする必要があります。 この設定の主なアプリケーションにより、ホスト上のリスナーは Teredo IPv6 アドレスを使用してグローバルにアドレス可能にすることができます。 新しいルールでは、EdgeTraversal プロパティは既定で無効になっています。 可能な値は、`notConfigured`、`blocked`、`allowed` です。|
|localUserAuthorizations|String|アプリコンテナーに対して承認されたローカルユーザーのリストを指定します。 これは、セキュリティ記述子定義言語 (SDDL) 形式の文字列です。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsFirewallRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsFirewallRule",
  "displayName": "String",
  "description": "String",
  "packageFamilyName": "String",
  "filePath": "String",
  "serviceName": "String",
  "protocol": 1024,
  "localPortRanges": [
    "String"
  ],
  "remotePortRanges": [
    "String"
  ],
  "localAddressRanges": [
    "String"
  ],
  "remoteAddressRanges": [
    "String"
  ],
  "profileTypes": "String",
  "action": "String",
  "trafficDirection": "String",
  "interfaceTypes": "String",
  "edgeTraversal": "String",
  "localUserAuthorizations": "String"
}
```



