---
title: deviceEnrollmentType 列挙型
description: モバイルデバイスを管理に追加する方法には、次のようなものがあります。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: enumPageType
ms.openlocfilehash: 0b53d279863ad3e17691b9e4d0397ba5f7d1b408
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36372084"
---
# <a name="deviceenrollmenttype-enum-type"></a>deviceEnrollmentType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

モバイルデバイスを管理に追加する方法には、次のようなものがあります。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|不明|.0|既定値。登録の種類は収集されませんでした。|
|userEnrollment|1-d|BYOD channel 経由のユーザー主導型の登録。|
|deviceEnrollmentManager|pbm-2|デバイス登録マネージャーアカウントを使用したユーザー登録。|
|appleBulkWithUser|1/3|ユーザーチャレンジを使用した Apple 一括登録。 (DEP、Apple Configurator)|
|appleBulkWithoutUser|2/4|ユーザーチャレンジなしの Apple 一括登録。 (DEP、Apple Configurator、モバイル構成)|
|windowsAzureADJoin|5|Windows 10 Azure AD Join。|
|windowsBulkUserless|シックス|Windows 10 証明書を使用した ICD による一括登録。|
|windowsAutoEnrollment 登録|7|Windows 10 の自動登録。 (作業アカウントの追加)|
|windowsBulkAzureDomainJoin|8 |Windows 10 一括 Azure AD Join。|
|windowsCoManagement|9 |Windows 10 の共同管理は、自動操縦またはグループポリシーによって開始されます。|



