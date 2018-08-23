---
title: アカウント管理 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: アカウント管理 API では、アカウント情報へのアクセスを提供し、アカウントの変更の通知をサポートします。 この API のクライアントとしてメール プロバイダーの次の操作を行います。
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799297"
---
# <a name="about-the-account-management-api"></a>アカウント管理 API について

アカウント管理 API では、アカウント情報へのアクセスを提供し、アカウントの変更の通知をサポートします。 この API のクライアントとしてメール プロバイダーの次の操作を行います。
  
1. アカウントへのアクセスを管理し、アカウントの変更に関する通知を設定するには、 [IOlkAccountManager](iolkaccountmanager.md)を使用します。 
    
2. 実装し、アカウントの変更に関する通知を送信する[IOlkAccountNotify](iolkaccountnotify.md)を使用します。 
    
3. [IOlkEnum](iolkenum.md)を使用して、アカウントを列挙します。 
    
4. 取得し、プロパティとその他のアカウント情報を設定するには、 [IOlkAccount](iolkaccount.md)を使用します。 クライアントでは、個別のアカウントにアクセスするには、 [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md)または[IOlkEnum::GetNext](iolkenum-getnext.md)では、このインターフェイスを取得します。 
    
5. 実装し、アカウントのプロファイルの名前と現在の MAPI セッションを取得するなど、アカウント マネージャー ヘルパー機能を提供する[IOlkAccountHelper](iolkaccounthelper.md)を使用します。 
    
6. 実装し、 **IOlkAccountManager**、 **IOlkAccountNotify**、および**IOlkAccount**でのエラーに関する追加情報を提供する[IOlkErrorUnknown](iolkerrorunknown.md)を使用します。 

##  <a name="account-management-api-components"></a>アカウント管理 API のコンポーネント

アカウント管理 API は、次の定義、データ型、インターフェイス、プロパティ、およびプロパティの名前を提供します。
  
### <a name="definitions"></a>定義
  
- [定数 (アカウント管理 API)](constants-account-management-api.md)
    
### <a name="data-types"></a>データ型
  
- [ACCT_BIN](acct_bin.md)
    
- [ACCT_VARIANT](acct_variant.md)
    
### <a name="interfaces"></a>インターフェイス
  
- [IOlkAccount](iolkaccount.md)
    
- [IOlkAccountHelper](iolkaccounthelper.md)
    
- [IOlkAccountManager](iolkaccountmanager.md)
    
- [IOlkAccountNotify](iolkaccountnotify.md)
    
- [IOlkEnum](iolkenum.md)
    
- [IOlkErrorUnknown](iolkerrorunknown.md)
    
### <a name="named-properties"></a>名前付きプロパティ
  
- [PidLidInternetAccountName](pidlidinternetaccountname.md)
    
- [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a>プロパティ
  
- [PidTagNextSendAcct](pidtagnextsendacct.md)
    
- [PidTagPrimarySendAccount](pidtagprimarysendaccount.md)
    
- [PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md)
    
- [PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md)
    
- [PROP_ACCT_ID](prop_acct_id.md)
    
- [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)
    
- [PROP_ACCT_NAME](prop_acct_name.md)
    
- [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)
    
- [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md)
    
- [PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md)
    
- [PROP_ACCT_STAMP](prop_acct_stamp.md)
    
- [PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)
    
- [PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md)
    
- [PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md)
    
- [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)
    
- [PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md)
    

