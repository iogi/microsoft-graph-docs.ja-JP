---
title: Office 365 グループ アクティビティ レポート
description: 組織で Office 365 のグループの活動の洞察を獲得でき、Office 365 のグループの数が表示されるを参照してください作成され、使用されます。
ms.openlocfilehash: fed72d93c9a5fcdf5f6c30cf122ce4d838662a01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27069758"
---
# <a name="office-365-groups-activity-reports"></a>Office 365 グループ アクティビティ レポート

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

組織で Office 365 のグループの活動の洞察を獲得でき、Office 365 のグループの数が表示されるを参照してください作成され、使用されます。

> **注:** 別のレポートのビューとレポート名についての詳細は、「[Office 365 レポート: Office 365 グループ](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40)」を参照してください。

## <a name="reports"></a>レポート

| 関数                                 | CSV の戻り値の型 | JSON の戻り値の型                         | 説明                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [グループの詳細を取得する](../api/reportroot-getoffice365groupsactivitydetail.md) | Stream          | [office365GroupsActivityDetail](../resources/office365groupsactivitydetail.md) | グループ別の Office 365 グループ アクティビティに関する詳細を取得します。 |
| [アクティビティの数を取得する](../api/reportroot-getoffice365groupsactivitycounts.md) | Stream          | [office365GroupsActivityCounts](../resources/office365groupsactivitycounts.md) | グループ ワークロード全体のグループ活動の数を取得します。 |
| [グループの数を取得する](../api/reportroot-getoffice365groupsactivitygroupcounts.md) | Stream          | [office365GroupsActivityGroupCounts](../resources/office365groupsactivitygroupcounts.md) | グループの日次合計数と、そのうちのアクティブなグループの数を、電子メールでの会話、Yammer の投稿、SharePoint ファイルのアクティビティに基づいて取得します。 |
| [ストレージを取得する](../api/reportroot-getoffice365groupsactivitystorage.md) | Stream          | [office365GroupsActivityStorage](../resources/office365groupsactivitystorage.md) | すべてのグループ メールボックスとグループ サイトで使用されているストレージの合計を取得します。 |
| [ファイルの数を取得する](../api/reportroot-getoffice365groupsactivityfilecounts.md) | Stream          | [office365GroupsActivityFileCounts](../resources/office365groupsactivityfilecounts.md) | Office 365 グループに関連付けられたグループ サイト全体での、ファイルの合計数と、そのうちのアクティブにされたファイルの数を取得します。 |