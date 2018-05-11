# <a name="update-rule"></a><span data-ttu-id="8cfe2-101">ルールを更新する</span><span class="sxs-lookup"><span data-stu-id="8cfe2-101">Update rule</span></span>


<span data-ttu-id="8cfe2-102">[messageRule](../resources/messagerule.md) オブジェクトの書き込み可能なプロパティを変更し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-102">Change writable properties on a rule and save the changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="8cfe2-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="8cfe2-103">Permissions</span></span>
<span data-ttu-id="8cfe2-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8cfe2-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="8cfe2-106">Permission type</span></span>      | <span data-ttu-id="8cfe2-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="8cfe2-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8cfe2-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="8cfe2-108">Delegated (work or school account)</span></span> | <span data-ttu-id="8cfe2-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8cfe2-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="8cfe2-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="8cfe2-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8cfe2-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8cfe2-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="8cfe2-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="8cfe2-112">Application</span></span> | <span data-ttu-id="8cfe2-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8cfe2-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="8cfe2-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="8cfe2-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/inbox/messagerules/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="8cfe2-115">オプションの要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="8cfe2-115">Optional request headers</span></span>
| <span data-ttu-id="8cfe2-116">名前</span><span class="sxs-lookup"><span data-stu-id="8cfe2-116">Name</span></span>       | <span data-ttu-id="8cfe2-117">説明</span><span class="sxs-lookup"><span data-stu-id="8cfe2-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="8cfe2-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="8cfe2-118">Authorization</span></span>  | <span data-ttu-id="8cfe2-p102">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="8cfe2-121">要求本文</span><span class="sxs-lookup"><span data-stu-id="8cfe2-121">Request body</span></span>
<span data-ttu-id="8cfe2-p103">要求本文で、更新する関連フィールドの値を指定します。要求本文に含まれない既存のプロパティは、以前の値のままになるか、他のプロパティ値の変化に基づいて再計算されます。最適なパフォーマンスを得るためには、変更されていない既存の値を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8cfe2-125">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8cfe2-125">Property</span></span>     | <span data-ttu-id="8cfe2-126">型</span><span class="sxs-lookup"><span data-stu-id="8cfe2-126">Type</span></span>   |<span data-ttu-id="8cfe2-127">説明</span><span class="sxs-lookup"><span data-stu-id="8cfe2-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8cfe2-128">actions</span><span class="sxs-lookup"><span data-stu-id="8cfe2-128">Actions</span></span> | [<span data-ttu-id="8cfe2-129">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="8cfe2-129">MessageRuleActions</span></span>](../resources/messageruleactions.md) | <span data-ttu-id="8cfe2-130">該当する条件が満たされた場合にメッセージに対して実行されるアクション。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-130">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="8cfe2-131">conditions</span><span class="sxs-lookup"><span data-stu-id="8cfe2-131">Conditions</span></span> | [<span data-ttu-id="8cfe2-132">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="8cfe2-132">MessageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="8cfe2-133">該当するルール アクションをトリガーするために満たす必要のある条件。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-133">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="8cfe2-134">displayName</span><span class="sxs-lookup"><span data-stu-id="8cfe2-134">displayName</span></span> | <span data-ttu-id="8cfe2-135">String</span><span class="sxs-lookup"><span data-stu-id="8cfe2-135">String</span></span> | <span data-ttu-id="8cfe2-136">ルールの表示名。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-136">The display name of the rule.</span></span> |
| <span data-ttu-id="8cfe2-137">exceptions</span><span class="sxs-lookup"><span data-stu-id="8cfe2-137">exceptions</span></span> | [<span data-ttu-id="8cfe2-138">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="8cfe2-138">MessageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="8cfe2-139">ルールの例外条件。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-139">Represents exception conditions for the rule.</span></span> |
| <span data-ttu-id="8cfe2-140">isEnabled</span><span class="sxs-lookup"><span data-stu-id="8cfe2-140">IsEnabled</span></span> | <span data-ttu-id="8cfe2-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="8cfe2-141">Boolean</span></span> | <span data-ttu-id="8cfe2-142">メッセージに対するルールの適用が有効になっているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-142">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="8cfe2-143">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="8cfe2-143">IsReadOnly</span></span> | <span data-ttu-id="8cfe2-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="8cfe2-144">Boolean</span></span> | <span data-ttu-id="8cfe2-145">ルールが読み取り専用のため、ルールの REST API による変更や削除ができないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-145">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="8cfe2-146">sequence</span><span class="sxs-lookup"><span data-stu-id="8cfe2-146">Sequence</span></span> | <span data-ttu-id="8cfe2-147">Int32</span><span class="sxs-lookup"><span data-stu-id="8cfe2-147">Int32</span></span> | <span data-ttu-id="8cfe2-148">他のルールもある中で、そのルールが実行される順序を示します。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-148">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="response"></a><span data-ttu-id="8cfe2-149">応答</span><span class="sxs-lookup"><span data-stu-id="8cfe2-149">Response</span></span>
<span data-ttu-id="8cfe2-150">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文に更新後の [messageRule](../resources/messagerule.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-150">If successful, this method returns a `200 OK` response code and updated [ChartSeries](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8cfe2-151">例</span><span class="sxs-lookup"><span data-stu-id="8cfe2-151">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8cfe2-152">要求</span><span class="sxs-lookup"><span data-stu-id="8cfe2-152">Request</span></span>
<span data-ttu-id="8cfe2-153">次の例では、ルールの名前、「[ルールを取得する](messagerule_get.md)」の[例](messagerule_get.md#example)のルールに対して実行するアクションを転送元からアドレスを変更し、その重要度を高くマークします。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-153">The following example changes the name of the rule, and the actions to be taken for that rule in the last example, from forwarding to an address to marking its importance as high.</span></span> 
<!-- {
  "blockType": "request",
  "name": "update_messagerule"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/mailfolders/inbox/messagerules('AQAAAJ5dZqA=')

Content-type: application/json

{
    "displayName": "Important from partner",
    "actions": {
        "markImportance": "high"
     }
} 
```
##### <a name="response"></a><span data-ttu-id="8cfe2-154">応答</span><span class="sxs-lookup"><span data-stu-id="8cfe2-154">Response</span></span>
<span data-ttu-id="8cfe2-p104">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="8cfe2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Me/mailFolders('inbox')/messageRules/$entity",
  "id":"AQAAAJ5dZqA=",
  "displayName":"Important from partner",
  "sequence":2,
  "isEnabled":true,
  "hasError":false,
  "isReadOnly":false,
  "conditions":{
    "senderContains":[
      "ADELE"
    ]
  },
  "actions":{
    "markImportance": "high"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->