---
title: アドレス帳プロバイダーのオプション機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ffdd1203316b2c80aba34c980745a0330ec19888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801694"
---
# <a name="optional-features-for-address-book-providers"></a>アドレス帳プロバイダーのオプション機能

  
  
**適用対象**: Outlook 
  
アドレス帳プロバイダーの多くのオプション機能があります。 さらに一般的に実装された機能は次のとおりです。
  
- 別のプロバイダーのコンテナーに追加するのには、コンテナーの 1 つのエントリを許可することでは、外部のプロバイダーとして動作しています。
    
- コンテナーのいずれかに別のプロバイダーからのエントリを追加するのには、ホスト プロバイダーとして動作しています。
    
- 高度な検索します。
    
- プレフィックスのテーブルの内容をスクロールします。
    
- 配布リストをサポートします。
    
- イベント通知をサポートします。
    
次の表には、これらのオプションの機能とそれらを実装する方法について簡単にについて説明します。
  
|**機能**|**実装する方法**|
|:-----|:-----|
|受信者の一覧メッセージのエントリを作成するためのテンプレートを指定します。  <br/> |[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)メソッドを実装します。 詳細については、[一時テーブル](one-off-tables.md)と[一時テーブルを実装する](implementing-one-off-tables.md)を参照してください。  <br/> |
|名前付きの単位にグループの受信者  <br/> |配布リストのプロパティをサポートして導入することにより、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)インタ フェースです。  <br/> |
|別のプロバイダーのコンテナーに追加するエントリを許可することで外部アドレス帳プロバイダーとして動作します。  <br/> | ホスト プロバイダーにデータ バインディング コードをサポートしてください。  <br/>  ユーザーおよび配布リストをメッセージに**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートします。 詳細については、[アドレス帳の識別子](address-book-identifiers.md)を参照してください。  <br/>  [IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドを実装します。 詳細については、[外部のアドレス帳プロバイダーとしての機能](acting-as-a-foreign-address-book-provider.md)を参照してください。  <br/> |
|別のプロバイダーからのエントリを挿入することによって、ホストのアドレス帳プロバイダーとして機能します。  <br/> |[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出すことによってコードに外部プロバイダーからのデータ バインディングをサポートします。 詳細については、[ホストのアドレス帳プロバイダーとしての機能](acting-as-a-host-address-book-provider.md)を参照してください。  <br/> |
|スクロールを付ける  <br/> |コンテナーの内容のテーブルの制約をサポートします。 詳細については、[制限の詳細](about-restrictions.md)を参照してください。  <br/> |
|高度なコンテナー内の検索  <br/> |コンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) のプロパティをサポートします。 詳細については、[高度な検索を実装する](implementing-advanced-searching.md)を参照してください。  <br/> |
|イベント通知  <br/> |[IABLogon::Advise](iablogon-advise.md)メソッドと[IABLogon::Unadvise](iablogon-unadvise.md)メソッドを実装します。 詳細については、 [MAPI でのイベント通知](event-notification-in-mapi.md)[イベント通知のサポート](supporting-event-notification.md)を参照してください。  <br/> |
   
イベントの通知、 **IABLogon::Advise**メソッドが呼び出される MAPI によってクライアントは、ユーザーまたは配布リストをメッセージのコンテナーのいずれかの通知を登録する**IAddrBook::Advise**を呼び出すと。 ただし、イベント通知をサポートしているが省略可能であるために、これらのメソッドから MAPI_E_NO_SUPPORT を取得できます。 ただし、MAPI には少なくとも、内容のテーブルの通知をサポートしているすべての種類の値を追加するのには_fnevSearchComplete_と_fnevCriticalError_のイベントを除くオブジェクトの通知をサポートすることをお勧めはお勧めします。 
  

