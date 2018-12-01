---
title: DriveItem のバージョンを一覧表示
description: OneDrive と SharePoint は、ファイルの履歴を保持するように構成できます。
ms.openlocfilehash: a0092fa244543fbc2233cd9de20ecebd2938fd79
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27069220"
---
# <a name="listing-versions-of-a-driveitem"></a>DriveItem のバージョンを一覧表示

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

OneDrive と SharePoint は、ファイルの履歴を保持するように構成できます。
サービスと構成に応じて、各編集に対する新しいバージョンを作成することができます。ファイルが保存されるたびに作成するか、手動で作成するか、または全く作成しないこともできます。

ドキュメントの旧バージョンは、ユーザーまたは場所ごとに固有の場合がある管理者設定に応じて、一定期間保持することができます。

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | Files.Read、Files.ReadWrite、Files.Read.All、Files.ReadWrite.All、Sites.Read.All、Sites.ReadWrite.All    |
|委任 (個人用 Microsoft アカウント) | Files.Read、Files.ReadWrite、Files.Read.All、Files.ReadWrite.All    |
|アプリケーション | Files.Read.All、Files.ReadWrite.All、Sites.Read.All、Sites.ReadWrite.All |


## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions
GET /groups/{group-id}/drive/{item-id}/versions
GET /me/drive/items/{item-id}/versions
GET /sites/{site-id}/drive/items/{item-id}/versions
GET /users/{user-id}/drive/items/{item-id}/versions
```

## <a name="response"></a>応答

成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [DriveItemVersion](../resources/driveitemversion.md) オブジェクトのコレクションを返します。


## <a name="example"></a>例

この例では、現在のユーザーのドライブ内のファイルのそのバージョンを取得します。

### <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "request", "name": "get-previous-versions", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/versions
```

### <a name="response"></a>応答

バージョンのコレクションを返します。

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItemVersion)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value":
  [
    {
      "id": "3.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-14T12:34:53.912Z",
      "size": 123
    },
    {
      "id": "2.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-11T10:21:03.000Z",
      "size": 62
    },
    {
      "id": "1.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-10T15:20:01.125Z",
      "size": 16
    }
  ]
}
```

## <a name="remarks"></a>備考

OneDrive は、ファイルの旧バージョンの完全なメタデータを保持しません。

アプリがファイルの利用可能なバージョンのリストを取得すると、[DriveItemVersion](../resources/driveitemversion.md) リソースが返され、特定のバージョンに関する利用可能な情報が提供されます。


<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->