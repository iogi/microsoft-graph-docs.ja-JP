# <a name="skype-for-business-organizer-activity-reports"></a>Skype for Business 開催者アクティビティ レポート

Skype for Business 開催者アクティビティ レポートを使用して、組織全体で開催した会議アクティビティの詳細を取得できます。 これらの詳細は、組織のための調査、計画、その他のビジネスの意思決定の際に非常に役立ちます。

> **注:** 別のレポートのビューとレポート名についての詳細は、「[Office 365 レポート: Skype for Business 電話会議の開催者のアクティビティ](https://support.office.com/client/Skype-for-Business-Online-conference-organized-activity-03a255d4-0e1d-4b24-b73d-7a62fae36254)」を参照してください。

## <a name="reports"></a>レポート

| 関数                                 | 戻り値の型 | 説明                              |
| :--------------------------------------- | :---------- | :--------------------------------------- |
| [アクティビティの数を取得する](../api/reportroot_getskypeforbusinessorganizeractivitycounts.md) | Stream      | 組織内のユーザーが開催、企画した電話会議セッションの数と種類に関する使用状況の傾向を取得します。 会議セッションの種類には、IM、オーディオ/ビデオ、アプリケーション共有、Web、サード パーティへのダイヤルイン/ダイヤルアウト、Microsoft へのダイヤルイン/ダイヤルアウトなどがあります。 |
| [ユーザーの数を取得する](../api/reportroot_getskypeforbusinessorganizeractivityusercounts.md) | Stream      | 一意のユーザー数と組織内のユーザーが開催、企画した電話会議セッションの数と種類に関する使用傾向を取得します。 会議セッションの種類には、IM、オーディオ/ビデオ、アプリケーション共有、Web、サード パーティへのダイヤルイン/ダイヤルアウト、Microsoft へのダイヤルイン/ダイヤルアウトなどがあります。 |
| [時間 (分) を取得する](../api/reportroot_getskypeforbusinessorganizeractivityminutecounts.md) | Stream      | 組織内のユーザーが開催、企画した電話会議セッションの長さ (分数) と種類に関する使用状況の傾向を取得します。 電話会議セッションの種類には、オーディオ/ビデオ、および Microsoft へのダイヤルインとダイヤルアウトがあります。 |
