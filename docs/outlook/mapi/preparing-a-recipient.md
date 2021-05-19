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
  
クライアント アプリケーションは、短期的なエントリ識別子を長期エントリ識別子に変換し、プロパティを追加、変更、または並べ替えることによって受信者を準備します。 メッセージに関係のないメッセージまたは受信者の受信者リストの一部である受信者を準備できます。 通常、クライアントは [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) を直接呼び出して、短期エントリ識別子を共通のアドレス ダイアログ ボックスに含まれる受信者の長期エントリ識別子に変換します。 送信メッセージに関連付けられている受信者の場合、受信者の準備は名前解決プロセスによって処理されます。 
  
受信者のリストを準備するには **、IAddrBook::P repareRecips を呼び出します**。 **PrepareRecips は**[、ADRLIST](adrlist.md)構造とプロパティ タグのリストを受け入れる。 **ADRLIST 構造には**、準備する受信者が含まれるのに対し、プロパティ タグリストは各受信者がサポートする必要があるプロパティを表します。 **PrepareRecips は** 、プロパティ タグ リストに含まれるプロパティを **ADRLIST** 構造体の先頭に配置します。 リスト内のプロパティの 1 つが **ADRLIST** 構造から欠落している場合、MAPI はアドレス帳プロバイダーを呼び出して提供します。 長期エントリ識別子のみを確認する必要がある場合は  _、lpSPropTagArray_ パラメーターに NULL を渡します。 
  
たとえば、5 人の受信者を操作するとします。 5 人の受信者すべてが **ADRLIST 構造に表示** され、次のプロパティが次の順序で表示されます。 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
最初の 2 つの受信者の **ADRLIST** 構造には、他の 3 つのプロパティが含まれています。 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
すべての受信者が最初の **3** つのプロパティ **PR_ADDRTYPE、PR_ENTRYID、** および PR_HOME_TELEPHONE_NUMBER ([PidTagHomeTelephoneNumber)](pidtaghometelephonenumber-canonical-property.md)として持つ必要があるため、これらのプロパティを持つプロパティ タグ配列を作成し、そのプロパティと **ADRLIST** 構造体を **PrepareRecips** に渡します。  **PrepareRecips は**、現在 **ADRLIST** 構造の一部ではないので、各受信者の **IMAPIProp::GetProps** メソッドを呼び出して PR_HOME_TELEPHONE_NUMBER を取得します。 **PrepareRecips が返** される場合、受信者リストは、受信者ごとに最初に表示される **ADRLIST** 構造に含まれるプロパティを持つ、結合された受信者の一覧を表します。 
  
受信者 1 と受信者 2 の受信者リストには、次の順序でプロパティが含まれます。
  
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
    
受信者 3、4、および 5 の受信者リストには、次の順序でプロパティが含まれます。
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
**IAddrBook::P repareRecips** を呼び出してプロパティを処理する代わりに、各受信者の [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出し、必要に応じて [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。 受信者が 1 人しか関与しない場合は、どちらの方法でも十分です。 ただし、複数の受信者が関係する場合は **、IMAPIProp** メソッドではなく **PrepareRecips** を呼び出すことによって時間が節約され、リモートで操作している場合は、多くのリモート プロシージャ呼び出しが実行されます。 **PrepareRecips は** 1 回の呼び出しですべての受信者を処理しますが **、GetProps** と **SetProps** は受信者ごとに 1 回の呼び出しを行います。 
  

