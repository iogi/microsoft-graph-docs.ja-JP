<a id="domaindnsmxrecord-resource-type" class="xliff"></a>
# domainDnsMxRecord リソースの種類

テナント内の特定のドメインの DNS ゾーン ファイルに追加された MX レコードを表します。[DomainDnsRecord](domaindnsrecord.md) エンティティから継承されます。

<a id="methods" class="xliff"></a>
## メソッド
このリソースへの直接クエリはサポートされていません。ドメイン サービス レコードのクエリを実行する方法の詳細については、[ドメイン](domain.md)のトピックを参照してください。

<a id="properties" class="xliff"></a>
## プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|String| このエンティティに割り当てられた一意の識別子。null 許容ではありません。読み取り専用です。|
|isOptional|Boolean| False の場合、MX レコードは Microsoft オンライン サービスでドメインを正しく操作するために、DNS ホストで顧客によって構成されている必要があります。 |
|label|String| DNS ホストで MX レコードの *alias/host/name* プロパティを構成する場合に使用される値です。 |
|mailExchange|String| DNS ホストで MX レコードの *answer/destination/value* を構成する場合に使用される値です。|
|preference|Int32| DNS ホストで MX レコードの *Preference/Priority* プロパティを構成する場合に使用される値です。 |
|recordType|String| DNS レコードの種類。この値は常に *Mx* です。キー |
|supportedService|String| Microsoft オンライン サービスまたはこの MX レコードに依存している機能。</br></br>次のいずれかの値を指定できます。**null**、*Email*、*Sharepoint*、*EmailInternalRelayOnly*、*OfficeCommunicationsOnline*、*SharePointDefaultDomain*、*FullRedelegation*、*SharePointPublic*、*OrgIdAuthentication*、*Yammer*、*Intune* |
|ttl|Int32| DNS ホストで MX レコードの *Time To Live (ttl)* プロパティを設定するときに使用する値。null 許容ではありません |

<a id="relationships" class="xliff"></a>
## リレーションシップ
なし

<a id="json-representation" class="xliff"></a>
## JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsMxRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "mailExchange": "String",
  "preference": 1024,
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsMxRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->