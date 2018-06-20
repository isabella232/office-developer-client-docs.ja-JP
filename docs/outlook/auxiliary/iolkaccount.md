---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: dc802d8fef0d90672428c8bfa3662a2734637d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799445"
---
# <a name="iolkaccount"></a>IOlkAccount

取得および設定のプロパティおよびその他のアカウント情報をサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
|提供元:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md)と[IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |型指定されたアカウントのカテゴリを取得します。  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |指定したアカウントのプロパティの値を取得します。 次の表のプロパティを参照してください。  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |指定したアカウントのプロパティの値を設定します。 次の表のプロパティを参照してください。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |**IOlkAccount**インターフェイスによって割り当てられたメモリを解放します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |レジストリ ストアに書き込むことによって、アカウント オブジェクトに変更をコミットします。  <br/> |
   
## <a name="properties"></a>プロパティ

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |アカウントの既定の配信フォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |アカウントの既定の配信ストアのエントリ ID を表します。  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Outlook 2000 および Outlook の以前のバージョンでは、アカウントの識別子を返します。  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |アカウントが Microsoft Exchange のアカウントである場合は true。  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Outlook 2002 以降のバージョンの Outlook でアカウントの識別子を返します。  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |アカウント名を返します。  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |アカウントの基本設定を格納するプロファイル] セクションに一意の識別子 (UID) を取得します。  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |アカウントの「送信」タイムスタンプをを返します。  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |アカウントの送信済みアイテムの既定のフォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |アカウントのタイムスタンプを返します。  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |ユーザーの表示名を返します。  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |アカウントの電子メール アドレスを指定します。  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |取得または、アカウントのアドレス帳のエントリ ID を設定します。  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Microsoft Outlook を使用して必要な同期タスクを決定し、アカウントをサポートしないユーザー インターフェイス (UI) 要素を無効にするトランスポートの設定を表します。  <br/> |
   
## <a name="remarks"></a>備考

列挙子内の次のアカウントを取得するときに**IOlkAccount**と**IOlkEnum::GetNext**をサポートしているアカウントを検索するときは、 **IOlkAccountManager::FindAccount**によってこのインターフェイスが返されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

