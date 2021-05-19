---
title: アカウント管理 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: アカウント管理 API は、アカウント情報へのアクセスを提供し、アカウント変更の通知をサポートします。 この API のクライアントとして、メール プロバイダーは次の操作を行います。
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426250"
---
# <a name="about-the-account-management-api"></a>アカウント管理 API について

アカウント管理 API は、アカウント情報へのアクセスを提供し、アカウント変更の通知をサポートします。 この API のクライアントとして、メール プロバイダーは次の操作を行います。
  
1. [IOlkAccountManager を使用](iolkaccountmanager.md)してアカウントへのアクセスを管理し、アカウントの変更に関する通知を設定します。 
    
2. [IOlkAccountNotify](iolkaccountnotify.md)を実装して使用して、アカウントの変更に関する通知を送信します。 
    
3. [IOlkEnum を使用して](iolkenum.md)アカウントを列挙します。 
    
4. [IOlkAccount を使用して](iolkaccount.md)、アカウントに関するプロパティや他の情報を取得および設定します。 クライアントは [、IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) または [IOlkEnum::GetNext](iolkenum-getnext.md) を使用してこのインターフェイスを取得して、個々のアカウントにアクセスします。 
    
5. [IOlkAccountHelper](iolkaccounthelper.md)を実装して使用して、アカウントのプロファイル名と現在の MAPI セッションを取得するなどのアカウント マネージャー ヘルパー機能を提供します。 
    
6. [IOlkErrorUnknown](iolkerrorunknown.md)を実装して使用して **、IOlkAccountManager、IOlkAccountNotify、** および **IOlkAccount** のエラーに関する詳細な情報を **提供します**。 

##  <a name="account-management-api-components"></a>アカウント管理 API コンポーネント

アカウント管理 API には、次の定義、データ型、インターフェイス、名前付きプロパティ、およびプロパティが含まれます。
  
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
    

