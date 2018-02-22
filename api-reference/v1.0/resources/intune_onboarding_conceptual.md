# <a name="enroll-devices-for-management-in-intune"></a>Intune における管理用にデバイスを登録する

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://www.microsoft.com/ja-JP/cloud-platform/microsoft-intune-pricing)を持っている必要があります。

デバイス (Windows PC を含む) を登録して、Microsoft Intune でモバイル デバイス管理 (MDM) を有効にすることができます。 このトピックでは、Intune 管理における、いくつかのモバイル デバイスの登録方法について説明します。 デバイスを登録する方法は、デバイスの種類、所有権、必要な管理のレベルによって異なります。 "Bring Your Own Device" (BYOD) の登録により、ユーザーは、個人の電話、タブレット、PC を登録することができます。 会社所有のデバイス (COD) の登録により、リモートワイプ、共有デバイス、デバイスのユーザー アフィニティなどの管理シナリオが可能になります。

次の Graph リソースを使用して、Intune での登録を管理できます。

- [Apple プッシュ通知証明書](intune_devices_applepushnotificationcertificate.md)
- [監査アクター](intune_auditing_auditactor.md)
- [監査イベント](intune_auditing_auditevent.md)
- [監査のプロパティ](intune_auditing_auditproperty.md)
- [監査のリソース](intune_auditing_auditresource.md)
- [構成マネージャーのクライアントに対応した機能](intune_devices_configurationmanagerclientenabledfeatures.md)
- [共有の Apple デバイスのアクションの結果からユーザーを削除する](intune_devices_deleteuserfromsharedappledeviceactionresult.md)
- [検出されたアプリ](intune_devices_detectedapp.md)
- [デバイスのアクションの結果](intune_devices_deviceactionresult.md)
- [デバイス カテゴリ](intune_devices_devicecategory.md)
- [デバイスの Exchange アクセス状態の要約](intune_devices_deviceexchangeaccessstatesummary.md)
- [デバイスの位置情報](intune_devices_devicegeolocation.md)
- [デバイスの正常性構成証明の状態](intune_devices_devicehealthattestationstate.md)
- [デバイス管理のトラブルシューティング イベント](intune_troubleshooting_devicemanagementtroubleshootingevent.md)
- [デバイスの管理](intune_devices_devicemanagement.md)
- [デバイスの管理](intune_endpointprotection_devicemanagement.md)
- [デバイスの管理](intune_notification_devicemanagement.md)
- [デバイスの管理](intune_remoteassistance_devicemanagement.md)
- [デバイスの管理](intune_troubleshooting_devicemanagement.md)
- [デバイスの管理](intune_auditing_devicemanagement.md)
- [デバイスのオペレーティング システムの概要](intune_devices_deviceoperatingsystemsummary.md)
- [登録のトラブルシューティング イベント](intune_troubleshooting_enrollmenttroubleshootingevent.md)
- [ローカライズ済み通知メッセージ](intune_notification_localizednotificationmessage.md)
- [デバイスの検索アクションの結果](intune_devices_locatedeviceactionresult.md)
- [管理対象デバイスの概要](intune_devices_manageddeviceoverview.md)
- [管理対象デバイス](intune_devices_manageddevice.md)
- [通知メッセージ テンプレート](intune_notification_notificationmessagetemplate.md)
- [リモート アシスタンス パートナー](intune_remoteassistance_remoteassistancepartner.md)
- [リモート ロック アクションの結果](intune_devices_remotelockactionresult.md)
- [パスコードのリセット アクションの結果](intune_devices_resetpasscodeactionresult.md)
- [Windows のデバイス アカウントのアクション パラメーターの更新](intune_devices_updatewindowsdeviceaccountactionparameter.md)
- [ユーザー](intune_devices_user.md)
- [ユーザー](intune_troubleshooting_user.md)
- [Windows Defender のスキャン アクションの結果](intune_devices_windowsdefenderscanactionresult.md)
- [Windows のデバイス アカウント](intune_devices_windowsdeviceaccount.md)
- [Windows のデバイス AD アカウント](intune_devices_windowsdeviceadaccount.md)
- [Windows のデバイス Azure AD アカウント](intune_devices_windowsdeviceazureadaccount.md)