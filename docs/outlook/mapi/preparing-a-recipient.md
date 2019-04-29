---
title: 受信者の準備
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419878"
---
# <a name="preparing-a-recipient"></a>受信者の準備

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションは、短い用語のエントリ識別子を長期のエントリ識別子に変換して、プロパティの追加、変更、または並べ替えを行うことにより、受信者を事前に準備します。 メッセージに関連付けられていない受信者リストの一部である受信者を準備することができます。 通常、クライアントは[IAddrBook::P reparerecips](iaddrbook-preparerecips.md)を呼び出して、短い用語の入力識別子を、[共通アドレス] ダイアログボックスに含まれている受信者の長期エントリ識別子に変換します。 送信メッセージに関連付けられている受信者の場合、受信者の準備は名前解決プロセスによって処理されます。 
  
受信者の一覧を準備するには、 **IAddrBook::P reparerecips**を呼び出します。 **PrepareRecips**は、 [adrlist](adrlist.md)構造とプロパティタグのリストを受け入れます。 **adrlist**構造体には、各受信者がサポートするプロパティをプロパティタグリストが表す間に準備する受信者が含まれています。 **PrepareRecips**は、 **adrlist**構造の先頭に、プロパティタグリストに含まれるプロパティを配置しようとします。 リスト内のプロパティのいずれかが**adrlist**構造に欠落している場合、MAPI はアドレス帳プロバイダーを呼び出して指定します。 長期のエントリ識別子のみをチェックする必要がある場合は、 _lpSPropTagArray_パラメーターに NULL を渡します。 
  
たとえば、5人の受信者で作業しているとします。 すべての5人の受信者は、次の順序で、以下のプロパティを持つ**adrlist**構造に表示されます。 
  
1. **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
最初の2つの受信者の**adrlist**構造には、他に3つのプロパティが含まれています。 
  
1. **PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME**([PidTagSurname](pidtagsurname-canonical-property.md))
    
すべての受信者が最初の3つのプロパティ**PR_ADDRTYPE**、 **PR_ENTRYID**、および**PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)) を必要とするため、これらのプロパティを使用してプロパティタグ配列を作成し、渡します。**PrepareRecips**には、これと**adrlist**構造があります。 **PrepareRecips**は、現在**adrlist**構造体の一部ではないため、各受信者の**imapiprop:: GetProps**メソッドを呼び出して、 **PR_HOME_TELEPHONE_NUMBER**を取得します。 **PrepareRecips**が戻ると、受信者リストは、各受信者に対して最初に表示される**adrlist**構造に含まれるプロパティを持つ受信者の結合されたリストを表します。 
  
受信者1および2の受信者の一覧には、次の順序でプロパティが含まれています。
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
8. **PR_ACCOUNT**
    
9. **PR_GIVEN_NAME**
    
10. **PR_SURNAME**
    
受信者3、4、および5の受信者の一覧には、次の順序でプロパティが含まれています。
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
**IAddrBook::P reparerecips**を呼び出してプロパティを処理する代わりに、各受信者の[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出し、必要に応じて[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出します。 参加する受信者が1人だけの場合は、どちらの方法でも十分です。 ただし、複数の受信者が関係している場合は、 **imapiprop**メソッドではなく**PrepareRecips**を呼び出すと時間が節約され、リモートで操作している場合はリモートプロシージャコールの数が多くなります。 **PrepareRecips**は、すべての受信者を1回の呼び出しで処理し、 **GetProps**と**setprops**は各受信者に対して1つの呼び出しを行います。 
  

