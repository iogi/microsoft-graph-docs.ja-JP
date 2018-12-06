---
title: Microsoft Graph Security API の警告と SIEM の統合
description: Microsoft Graph Security API は、単一の REST エンドポイントを介して、すべての Microsoft セキュリティ製品 (Microsoft Graph Security プロバイダーと呼ばれる) から出力されるセキュリティの警告を管理する機能を提供します。 組織によっては、Azure Monitor によって Azure 固有のログ データが SIEM ソリューションに既に取り込まれている場合があります。 統合を簡略化するため、Microsoft Graph のセキュリティ API から使用できるセキュリティの警告は、ユーザーが自分のサブスクリプションに対して Azure Monitor 経由でプロビジョニングすることもできます。 Azure Monitor と SIEM ソリューションの統合が既に構成されている組織では、組織のセキュリティの警告を Azure Monitor で利用できる既存のデータに加えて簡単にストリーミングできます。
ms.openlocfilehash: ca2952163ab8894cae4c22f726b45b1be94a8b1f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092455"
---
# <a name="integrate-microsoft-graph-security-api-alerts-with-a-siem"></a>Microsoft Graph Security API の警告と SIEM の統合

Microsoft Graph Security API は、単一の REST エンドポイントを介して、すべての Microsoft セキュリティ製品 (Microsoft Graph Security プロバイダーと呼ばれる) から出力されるセキュリティの警告を管理する機能を提供します。 組織によっては、Azure Monitor によって Azure 固有のログ データが SIEM ソリューションに既に取り込まれている場合があります。 統合を簡略化するため、Microsoft Graph のセキュリティ API から使用できるセキュリティの警告は、ユーザーが自分のサブスクリプションに対して Azure Monitor 経由でプロビジョニングすることもできます。 Azure Monitor と SIEM ソリューションの統合が既に構成されている組織では、組織のセキュリティの警告を Azure Monitor で利用できる既存のデータに加えて簡単にストリーミングできます。

Azure Monitor は、複数の SIEM 製品へのコネクタをサポートします。 サポートされている SIEM 製品のリストについては、[イベント ハブへの監視データの送信](https://docs.microsoft.com/ja-JP/azure/monitoring-and-diagnostics/monitor-stream-monitoring-data-event-hubs#what-can-i-do-with-the-monitoring-data-being-sent-to-my-event-hub)を参照してください。 現在、Microsoft Graph Security API の統合は、[Splunk](https://splunkbase.splunk.com/) と [QRadar](https://www.ibm.com/us-en/marketplace/ibm-qradar-siem) で使用できます。

特定の SIEM ソリューションに対する Microsoft Graph Security API の統合については、次を参照してください。

- [Splunk](security-splunk-siemintegration.md)
- [QRadar](security-qradar-siemintegration.md)