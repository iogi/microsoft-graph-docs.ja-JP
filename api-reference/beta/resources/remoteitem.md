# <a name="remoteitem-resource-type"></a>RemoteItem リソースの種類

**remoteItem** リソースは、[**driveItem**](driveitem.md) が別のドライブに存在するアイテムを参照することを示します。このリソースは、ソース ドライブとターゲット項目の固有 ID を提供します。

非 null の **remoteItem** ファセットを持つ [**DriveItems**](driveitem.md)は、共有された、ユーザーの OneDrive に追加された、あるいは異質な項目のコレクション (検索結果など) から返される項目上にあるリソースです。

**注:**同じドライブにあるフォルダーとは異なり、リモート アイテムに移動された **driveItem** では、`id` 値が変更された可能性があります。

## <a name="json-representation"></a>JSON 表記

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.remoteItem", 
       "optionalProperties": ["name", "fileSystemInfo", "file", "folder"] } -->

```json
{
  "id": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "file": { "@odata.type": "microsoft.graph.file" },
  "fileSystemInfo": { "@odata.type": "microsoft.graph.fileSystemInfo" },
  "folder": { "@odata.type": "microsoft.graph.folder" },
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "name": "string",
  "package": { "@odata.type": "microsoft.graph.package" },
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "shared": { "@odata.type": "microsoft.graph.shared" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "size": 1024,
  "specialFolder": { "@odata.type": "microsoft.graph.specialFolder" },
  "webDavUrl": "url",
  "webUrl": "url"
}
```

## <a name="properties"></a>プロパティ

| プロパティ名        | 種類                                | 説明                                                                                                                                                       |
| :------------------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| createdBy            | [IdentitySet](identityset.md)       | その項目を作成したユーザー、デバイス、およびアプリケーションの ID。読み取り専用。                                                                                  |
| createdDateTime      | Timestamp                           | 項目作成の日付と時刻。読み取り専用。                                                                                                                        |
| file                 | [File](file.md)                     | リモート項目がファイルであることを示します。読み取り専用。                                                                                                              |
| fileSystemInfo       | [FileSystemInfo](filesysteminfo.md) | ローカル ファイル システムからのリモート項目についての情報。読み取り専用。                                                                                          |
| folder               | [Folder](folder.md)                 | リモート項目がフォルダーであることを示します。読み取り専用。                                                                                                            |
| id                   | String                              | ドライブ内のリモート項目の固有識別子です。読み取り専用。                                                                                                    |
| lastModifiedBy       | [IdentitySet](identityset.md)       | 最後にその項目を修正したユーザー、デバイス、およびアプリケーションの ID。読み取り専用。                                                                            |
| lastModifiedDateTime | Timestamp                           | アイテムが最後に変更された日時。読み取り専用。                                                                                                              |
| name                 | String                              | 省略可能。リモート項目のファイル名です。読み取り専用。                                                                                                                 |
| package              | [Package](package.md)               | 存在する場合、この項目がフォルダーやファイルではなくパッケージであることを示します。パッケージは、一部のコンテキストでのファイルのように、他のコンテキストではフォルダーのように扱われます。読み取り専用。 |
| parentReference      | [ItemReference](itemreference.md)   | リモート項目の親のプロパティです。読み取り専用です。                                                                                                           |
| shared               | [shared](shared.md)                 | アイテムが他のユーザーと共有されていることを示し、アイテムの共有状態に関する情報を提供します。読み取り専用です。                                       |
| sharepointIds        | [SharepointIds](sharepointids.md)   | OneDrive for Business と SharePoint 間の相互運用を、項目識別子の完全なセットと共に提供します。読み取り専用。                                          |
| size                 | Int64                               | リモート項目のサイズです。読み取り専用。                                                                                                                               |
| specialFolder        | [SpecialFolder](specialfolder.md)   | 現在のアイテムも特別なフォルダーとして使用可能な場合は、このファセットが返されます。読み取り専用。                                                                     |
| webDavUrl            | Url                                 | 項目の、DAV 互換性のある URL です。                                                                                                                                  |
| webUrl               | URL                                 | ブラウザーでリソースを表示するための URL。読み取り専用。                                                                                                         |

## <a name="remarks"></a>備考

**driveItem** のファセットに関する詳細については、「[driveItem](driveitem.md)」を参照してください。


<!-- {
  "type": "#page.annotation",
  "description": "remoteItem resource type provides a link to an item in another drive.",
  "keywords": "remoteitem symlink remote drive shared with me add to onedrive",
  "section": "documentation"
} -->