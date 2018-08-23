---
title: 受信者の準備
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 51241009262471bf30f7d71e3108b896bbce8df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803683"
---
# <a name="preparing-a-recipient"></a>受信者の準備

  
  
**適用対象**: Outlook 
  
クライアント アプリケーションでは、長期のエントリ id を短期的なエントリの識別子を変換して可能性のある追加、変更、またはプロパティの順序を変更して受信者を準備します。 メッセージの受信者のリストの一部である受信者またはメッセージに関連ではない受信者を準備できます。 通常、クライアントは、共通のアドレス] ダイアログ ボックスに含まれる受信者のエントリ id を長期的な短期的なエントリの識別子に変換するには、直接[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)を呼び出します。 送信メッセージに関連付けられている受信者、受信者の準備が名前解決処理によって処理されます。 
  
受信者の一覧を作成するには、 **IAddrBook::PrepareRecips**を呼び出します。 **PrepareRecips**は、 [ADRLIST](adrlist.md)構造体とプロパティ タグのリストを受け取ります。 **ADRLIST**構造体には、タグのプロパティ] ボックスの一覧は、各受信者をサポートする必要がありますプロパティを表すときに準備を整えるための受信者が含まれています。 **PrepareRecips**は、 **ADRLIST**構造体の先頭のプロパティ タグのリストに含まれているプロパティを配置しようとします。 **ADRLIST**構造体から、リスト内のプロパティのいずれかが表示されない、MAPI は、それらを提供するアドレス帳プロバイダーを呼び出します。 長期のエントリ id を確認する必要がある場合は、 _lpSPropTagArray_パラメーターに NULL を渡します。 
  
たとえば、5 人の受信者を使用するいるとします。 5 つのすべての受信者が、 **ADRLIST**構造体に次の順序で次のプロパティに表示されます。 
  
1. **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
他の 3 つのプロパティは、最初の 2 つの受信者の**ADRLIST**構造体に含まれます。 
  
1. **PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME**([PidTagSurname](pidtagsurname-canonical-property.md))
    
**PR_ADDRTYPE**、 **PR_ENTRYID**、および**PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)) の最初の 3 つのプロパティとして持つすべての受信者のため、これらのプロパティを持つプロパティ タグ配列を作成し、渡す**PrepareRecips**、 **ADRLIST**構造体です。 **PrepareRecips**は現在、 **ADRLIST**構造体の一部ではないので、 **PR_HOME_TELEPHONE_NUMBER**を取得するために、各受信者の**IMAPIProp::GetProps**メソッドが呼び出されます。 **PrepareRecips**が返されると、受信者の一覧は、受信者ごとに最初に表示する**ADRLIST**構造体に含まれているプロパティを使用して差し込み印刷の受信者の一覧を表します。 
  
1 と 2 の宛先の受信者の一覧には、次の順序でプロパティが含まれています。
  
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
    
3、4、および 5 の宛先の受信者の一覧には、次の順序でプロパティが含まれています。
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
プロパティを操作する**IAddrBook::PrepareRecips**を呼び出す代わりに、各受信者の[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、必要であれば、その[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドです。 のみ 1 人の受信者が関係する場合は、いずれかの技法は、満足のいく。 ただし、複数の受信者が含まれる場合は、時間の節約**IMAPIProp**メソッドではなく、 **PrepareRecips**を呼び出すと、している場合、リモートで多くのリモート プロシージャ コールします。 **GetProps**と**SetProps**は、受信者ごとに 1 つの呼び出しを行う一方、 **PrepareRecips**は 1 回の呼び出しのすべての受信者を処理します。 
  

