---
title: lanManagerAuthenticationLevel 列挙型
description: LanManagerAuthenticationLevel に指定できる値
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: enumPageType
ms.openlocfilehash: ade139765c9a362cd0c9f9365af0026c51ecb4ce
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36356726"
---
# <a name="lanmanagerauthenticationlevel-enum-type"></a>lanManagerAuthenticationLevel 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

LanManagerAuthenticationLevel に指定できる値

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|lmAndNltm|.0|LM & NTLM 応答を送信する|
|lmNtlmAndNtlmV2|1-d|LM & NTLM を送信する-ネゴシエートされる場合は NTLMv2 セッションセキュリティを使用する|
|lmAndNtlmOnly|pbm-2|LM & NTLM 応答のみを送信する|
|lmAndNtlmV2|1/3|LM & NTLMv2 応答のみを送信する|
|lmNtlmV2AndNotLm|2/4|LM & NTLMv2 応答のみを送信します。 LM を拒否する|
|lmNtlmV2AndNotLmOrNtm|5|LM & NTLMv2 応答のみを送信します。 NTLM & の LM を拒否する|



