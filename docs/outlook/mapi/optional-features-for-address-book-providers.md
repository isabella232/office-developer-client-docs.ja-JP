---
title: アドレス帳プロバイダーのオプション機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f5d8f0cd1b21f58e4e5c7d7ccd6cb19f3626c38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414572"
---
# <a name="optional-features-for-address-book-providers"></a>アドレス帳プロバイダーのオプション機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーには、多くのオプション機能があります。 一般的に実装されている機能には、次のようなものがあります。
  
- コンテナーの1つのエントリを別のプロバイダーのコンテナーに追加できるようにすることで、外部プロバイダーとして機能します。
    
- 別のプロバイダーからコンテナーの1つにエントリを追加することによって、ホストプロバイダーとして機能します。
    
- 高度な検索。
    
- 目次テーブルをスクロールするプレフィックス。
    
- 配布リストのサポート。
    
- イベント通知のサポート。
    
次の表に、これらのオプション機能とその実装方法を簡単に説明します。
  
|**機能**|**実装方法**|
|:-----|:-----|
|メッセージ受信者リストのエントリを作成するためのテンプレートを提供する  <br/> |[IABLogon:: getoneofftable](iablogon-getoneofftable.md)メソッドを実装します。 詳細については、「one-off[テーブル](one-off-tables.md)」と「 [1 回限りのテーブルの実装](implementing-one-off-tables.md)」を参照してください。  <br/> |
|受信者を指定の単位にグループ化する  <br/> |[idistlist: IMAPIContainer](idistlistimapicontainer.md)インターフェイスを実装することによって、配布リストのプロパティをサポートします。  <br/> |
|別のプロバイダーのコンテナーにエントリを追加できるようにすることにより、外部アドレス帳プロバイダーとして機能します。  <br/> | 次の方法でホストプロバイダーのデータへのバインドコードをサポートします。  <br/>  メッセージングユーザーおよび配布リストに対して**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートします。 詳細については、「[アドレス帳の識別子](address-book-identifiers.md)」を参照してください。  <br/>  [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドを実装します。 詳細については、「[外部アドレス帳プロバイダーとして機能する](acting-as-a-foreign-address-book-provider.md)」を参照してください。  <br/> |
|別のプロバイダーからエントリを挿入してホストアドレス帳プロバイダーとして機能する  <br/> |[imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーからのコードへのデータのバインドをサポートします。 詳細については、「[ホストアドレス帳プロバイダーとして機能する](acting-as-a-host-address-book-provider.md)」を参照してください。  <br/> |
|プレフィックスのスクロール  <br/> |コンテナーコンテンツテーブルの制限をサポートします。 詳細については、「[制限につい](about-restrictions.md)て」を参照してください。  <br/> |
|コンテナー内での高度な検索  <br/> |コンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティをサポートします。 詳細については、「[高度な検索の実装](implementing-advanced-searching.md)」を参照してください。  <br/> |
|イベント通知  <br/> |[IABLogon::](iablogon-advise.md)アドバイズおよび[IABLogon:: アドバイズ](iablogon-unadvise.md)中止メソッドを実装します。 詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」および「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。  <br/> |
   
イベント通知の場合、クライアントが**IAddrBook:: アドバイズ**を呼び出して、コンテナー、メッセージングユーザー、または配布リストのいずれかに通知を登録するときに、 **IABLogon:: アドバイズ**メソッドが MAPI によって呼び出されます。 ただし、イベント通知のサポートはオプションなので、これらのメソッドから MAPI_E_NO_SUPPORT を返すことができます。 ただし、MAPI では、少なくともコンテンツテーブルに対する通知をサポートしており、 _fnevSearchComplete_以外のすべての種類のオブジェクト通知と、値を追加する_fnevCriticalError_イベントをサポートすることをお勧めします。 
  

