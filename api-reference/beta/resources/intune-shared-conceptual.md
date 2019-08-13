---
title: Microsoft Intune での共有リソース-Microsoft Graph API
description: テナント組織の複数のワークフローをサポートする Intune エンドポイント (REST) の Microsoft Graph API の一覧を示します。
localization_priority: Normal
author: rolyon
ms.prod: intune
ms.openlocfilehash: 0d2252093f222f5908756f312c2e82d591c29920
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36372805"
---
# <a name="shared-resources-in-microsoft-intune"></a>Microsoft Intune での共有リソース

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでは、これらの API の使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

これらのエンドポイントは、Intune ワークフロー用の複数の Microsoft Graph API で使用されます。  特定のリソースを使用するために必要な目的、およびアクセス許可は、基になる呼び出しの特定のワークフローおよびコンテキストによって異なります。  さらに、特定のワークフローに対してのみ、特定のメソッド、プロパティ、およびアクションがサポートされます。

次の Graph リソースは、Intune ワークフロー間で共有されます。

- [アクションの状態](intune-shared-actionstate.md)
- [すべてのデバイスの割り当て先](intune-shared-alldevicesassignmenttarget.md)
- [すべてのライセンス ユーザーの割り当て先](intune-shared-alllicensedusersassignmenttarget.md)
- [コンプライアンスのステータス](intune-shared-compliancestatus.md)
- [デバイスおよびアプリ管理の割り当て先](intune-shared-deviceandappmanagementassignmenttarget.md)
- [デバイス アプリの管理](intune-shared-deviceappmanagement.md)
- [デバイス カテゴリ](intune-shared-devicecategory.md)
- [デバイスの登録のタイプ](intune-shared-deviceenrollmenttype.md)
- [デバイスの管理](intune-shared-devicemanagement.md)
- [デバイスのプラットフォームの種類](intune-shared-deviceplatformtype.md)
- [デバイスのタイプ](intune-shared-devicetype.md)
- [有効化](intune-shared-enablement.md)
- [有効化](intune-shared-enablement.md)
- [除外グループの割り当て先](intune-shared-exclusiongroupassignmenttarget.md)
- [グループの割り当て先](intune-shared-groupassignmenttarget.md)
- [インストール目的](intune-shared-installintent.md)
- [IP 範囲](intune-shared-iprange.md)
- [IPv4 の範囲](intune-shared-ipv4range.md)
- [IPv6 の範囲](intune-shared-ipv6range.md)
- [キー/値のペア](intune-shared-keyvaluepair.md)
- [MIME コンテンツ](intune-shared-mimecontent.md)
- [モバイル アプリのトラブルシューティング イベント](intune-shared-mobileapptroubleshootingevent.md)
- [プロキシ化されたドメイン](intune-shared-proxieddomain.md)
- [Report](intune-shared-report.md)
- [レポートのルート](intune-shared-reportroot.md)
- [アプリの状態の結果](intune-shared-resultantappstate.md)
- [RGB カラー](intune-shared-rgbcolor.md)
- [実行状態](intune-shared-runstate.md)
- [保存 UI 状態生成オプション](intune-shared-saveduistategenerationoptions.md)
- [URI](intune-shared-uri.md)
- [ユーザー](intune-shared-user.md)
- [VPP トークン アカウントのタイプ](intune-shared-vpptokenaccounttype.md)
- [VPP トークンのアクションのエラーの理由](intune-shared-vpptokenactionfailurereason.md)
- [Windows ドメイン参加の構成](intune-shared-windowsdomainjoinconfiguration.md)
