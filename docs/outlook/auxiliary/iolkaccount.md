---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 07b2669a88010ccb8d76d077f40d61ffdbe50d99
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625694"
---
# <a name="iolkaccount"></a>IOlkAccount

プロパティの取得と設定、およびアカウントに関するその他の情報をサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|実装元:  <br/> |Outlook  <br/> |
|提供元:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) と [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |指定したアカウントの種類とカテゴリを取得します。  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |指定したアカウント プロパティの値を取得します。 以下のプロパティの表を参照してください。  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |指定したアカウント プロパティの値を設定します。 以下のプロパティの表を参照してください。  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |**IOlkAccount** インターフェイスによって割り当てられたメモリを解放します。  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |レジストリ ストアに書き込み、アカウント オブジェクトに対する変更をコミットします。  <br/> |
   
## <a name="properties"></a>プロパティ

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |アカウントの既定の配信フォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |アカウントの既定の配信ストアのエントリ ID を表します。  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |2000 以前のバージョンOutlookのアカウント識別子を返Outlook。  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |アカウントが Microsoft アカウントの場合は true Exchangeします。  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |2002 以降のバージョンのアカウントOutlookをOutlookします。  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |アカウント名を返します。  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |アカウントの基本設定を格納するプロファイル セクションの一意識別子 (UID) を取得します。  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |アカウントの "送信" スタンプを返します。  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |アカウントの送信されたアイテムの既定のフォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |アカウント スタンプを返します。  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |ユーザーの表示名を返します。  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |アカウントの電子メール アドレスを指定します。  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |アカウントの UID [ACCT_BIN](acct_bin.md)含む、新しい構造をExchangeします。  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |アカウントのアドレス帳エントリ ID を取得または設定します。  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Microsoft Outlookが必要な同期タスクを決定し、アカウントがサポートしていないユーザー インターフェイス (UI) 要素を無効にするために使用するトランスポート設定を表します。  <br/> |
   
## <a name="remarks"></a>注釈

このインターフェイスは、列挙子で次のアカウントを取得するときに **、IOlkAccount** と **IOlkEnum::GetNext** をサポートするアカウントを検索するときに **、IOlkAccountManager::FindAccount** によって返されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)

