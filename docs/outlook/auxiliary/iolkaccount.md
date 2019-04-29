---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 007a44d13565889b4775f2d3fe9979685e1878b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425065"
---
# <a name="iolkaccount"></a>IOlkAccount

アカウントに関するプロパティやその他の情報の取得と設定をサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|実装元:  <br/> |Outlook  <br/> |
|提供元:  <br/> |[IOlkAccountManager:: findaccount](iolkaccountmanager-findaccount.md)および[IOlkEnum:: GetNext](iolkenum-getnext.md) <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
|[getaccountinfo](iolkaccount-getaccountinfo.md) <br/> |指定されたアカウントの種類とカテゴリを取得します。  <br/> |
|[getprop](iolkaccount-getprop.md) <br/> |指定されたアカウントのプロパティの値を取得します。 以下のプロパティの表を参照してください。  <br/> |
|[setprop](iolkaccount-setprop.md) <br/> |指定された account プロパティの値を設定します。 以下のプロパティの表を参照してください。  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |**IOlkAccount**インターフェイスによって割り当てられたメモリを解放します。  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |レジストリストアに書き込むことによって、アカウントオブジェクトへの変更をコミットします。  <br/> |
   
## <a name="properties"></a>プロパティ

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |アカウントの既定の配信フォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |アカウントの既定の配信ストアのエントリ ID を表します。  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |outlook 2000 およびそれ以前のバージョンの outlook でアカウント識別子を返します。  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |アカウントが Microsoft Exchange アカウントの場合は True。  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |outlook 2002 以降のバージョンの outlook でアカウント識別子を返します。  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |アカウント名を返します。  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |アカウントの設定を格納するプロファイルセクションの一意識別子 (UID) を取得します。  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |アカウント "send" スタンプを返します。  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |アカウントの送信アイテムの既定のフォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |アカウントスタンプを返します。  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |ユーザーの表示名を返します。  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |アカウントの電子メールアドレスを指定します。  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |アカウントのアドレス帳エントリ ID を取得または設定します。  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |必要な同期タスクを決定するために Microsoft Outlook で使用するトランスポート設定を表し、アカウントがサポートしていないユーザーインターフェイス (UI) 要素を無効にします。  <br/> |
   
## <a name="remarks"></a>注釈

このインターフェイスは、列挙子で次のアカウントを取得するときに、 **IOlkAccount**と**IOlkEnum:: GetNext**をサポートするアカウントを検索するときに、 **IOlkAccountManager:: findaccount**によって返されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

