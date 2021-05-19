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
  
アドレス帳プロバイダーには、多くのオプション機能があります。 より一般的に実装される機能のいくつかは次のとおりです。
  
- あるコンテナーからのエントリを別のプロバイダーのコンテナーに追加できるようにして、外部プロバイダーとして機能します。
    
- 別のプロバイダーのエントリをコンテナーの 1 つに追加して、ホスト プロバイダーとして機能します。
    
- 高度な検索。
    
- コンテンツ テーブルをスクロールするプレフィックス。
    
- 配布リストのサポート。
    
- イベント通知のサポート。
    
次の表では、これらのオプション機能とそれらを実装する方法について簡単に説明します。
  
|**機能**|**実装方法**|
|:-----|:-----|
|メッセージ受信者リストのエントリを作成するためのテンプレートを指定する  <br/> |[IABLogon::GetOneOffTable メソッドを実装](iablogon-getoneofftable.md)します。 詳細については [、「One-Off Tables」](one-off-tables.md) および [「Implementing One-Off参照してください](implementing-one-off-tables.md)。  <br/> |
|受信者を名前付きユニットにグループ化する  <br/> |[IDistList : IMAPIContainer インターフェイスを実装して、配布リストのプロパティをサポート](idistlistimapicontainer.md)します。  <br/> |
|別のプロバイダーのコンテナーにエントリを追加できるようにして、外部アドレス帳プロバイダーとして機能する  <br/> | 次の方法で、ホスト プロバイダーのデータへのバインド コードをサポートします。  <br/>  メッセージング ユーザー **PR_TEMPLATEID** 配布リストの [プロパティ (PidTagTemplateid)](pidtagtemplateid-canonical-property.md)プロパティをサポートします。 詳細については、「アドレス帳 [識別子」を参照してください](address-book-identifiers.md)。  <br/>  [IABLogon::OpenTemplateID メソッドを実装](iablogon-opentemplateid.md)します。 詳細については、「外部アドレス [帳プロバイダーとして機能する」を参照してください](acting-as-a-foreign-address-book-provider.md)。  <br/> |
|別のプロバイダーからのエントリを挿入してホスト アドレス帳プロバイダーとして機能する  <br/> |[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーからのコードへのデータのバインドをサポートします。 詳細については、「ホスト アドレス [帳プロバイダーとして機能する」を参照してください](acting-as-a-host-address-book-provider.md)。  <br/> |
|プレフィックスのスクロール  <br/> |コンテナー コンテンツ テーブルの制限をサポートします。 詳細については、「制限について [」を参照してください](about-restrictions.md)。  <br/> |
|コンテナー内の高度な検索  <br/> |コンテナーの **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティをサポートします。 詳細については、「高度な [検索の実装」を参照してください](implementing-advanced-searching.md)。  <br/> |
|イベント通知  <br/> |[IABLogon::Advise メソッドと](iablogon-advise.md) [IABLogon::Unadvise メソッドを](iablogon-unadvise.md)実装します。 詳細については [、「MAPI でのイベント通知」および「サポート](event-notification-in-mapi.md) イベント通知 [」を参照してください](supporting-event-notification.md)。  <br/> |
   
イベント通知の場合 **、IABLogon::Advise** メソッドは、クライアントが **IAddrBook::Advise** を呼び出して、コンテナー、メッセージング ユーザー、または配布リストのいずれかの通知に登録するときに MAPI によって呼び出されます。 ただし、サポート イベント通知はオプションなので、これらのメソッドからMAPI_E_NO_SUPPORT返します。 ただし、MAPI では、少なくともコンテンツ テーブルの通知をサポートすることをお勧めします。  _また、fnevSearchComplete_ および  _fnevCriticalError_ イベントを除くすべての種類のオブジェクト通知をサポートして値を追加することをお勧めします。 
  

