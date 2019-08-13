---
title: androidWorkProfileRequiredPasswordType 列挙型
description: Android の作業プロファイルに必要なパスワードの種類。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: enumPageType
ms.openlocfilehash: bde21830059ae73d24ed73d1537c91a68c048fef
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36334102"
---
# <a name="androidworkprofilerequiredpasswordtype-enum-type"></a>androidWorkProfileRequiredPasswordType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android の作業プロファイルに必要なパスワードの種類。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|deviceDefault|.0|デバイスの既定値。意図的ではありません。|
|lowSecurityBiometric 認証|1-d|低セキュリティ生体認証ベースのパスワードが必要です。|
|必須|pbm-2|必須です。|
|atLeastNumeric|1/3|少なくとも数値のパスワードが必要です。|
|numericComplex|2/4|数字の複雑なパスワードが必要です。|
|Atall Stアルファベット|5|少なくとも英字のパスワードが必要です。|
|atLeastAlphanumeric|シックス|少なくとも英数字のパスワードが必要です。|
|alphanumericWithSymbols|7|記号パスワードが必要な、少なくとも英数字。|



