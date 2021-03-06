# <a name="deviceenrollmentfailurereason-enum-type"></a>deviceEnrollmentFailureReason 列挙型

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

最高レベルの失敗は、登録にカテゴリーされます。
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|不明|0|既定値、失敗の理由は不明です。|
|認証|1|認証に失敗しました。|
|認証|2|呼び出しが認証されましたが、登録する権限がありませんでした。|
|accountValidation|3|登録用のアカウントを検証できませんでした。 (アカウントがブロックされています。登録が有効になっていません。)|
|userValidation|4|ユーザーは、valiudateされませんでした。 （ユーザーが存在しません、ライセンスがありません。）|
|deviceNotSupported|5|モバイル デバイスの管理用にデバイスはサポートされていません。|
|inMaintenance|6|アカウントは只今メンテナンス中です。|
|badRequest|7|クライアントが、サービスが認識/対応しない要求を送信しました。|
|featureNotSupported|8|この登録で用いられた特徴は、このアカウントではサポートされていません。|
|enrollmentRestrictionsEnforced|9|アドミニストレータにより構成された登録制限が、本登録をブロックしました。|
|clientDisconnected|10|クライアントがタイムアウトしたか、登録が、エンド ユーザーによって中止されました。|



