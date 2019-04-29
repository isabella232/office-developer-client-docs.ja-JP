---
title: 受信者リストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428215"
---
# <a name="creating-a-recipient-list"></a>受信者リストの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者リストは、各メッセージ受信者のプロパティ値構造 (メッセージの送信先) の配列を含む[adrlist](adrlist.md)構造です。 受信者は、人間のユーザー、コンピューター、またはフォルダーを表すことができます。 送信されるすべてのメッセージには、名前解決プロセスを通じて、少なくとも1人の受信者が必要です。 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが受信者のプロパティ値配列に含まれていることを確認するプロセスです。 
  
受信者のプロパティは、アドレス帳のプロパティとメッセージのプロパティの組み合わせです。 受信者のプロパティは、特定の受信者のすべてのメッセージに適用するか、または現在のメッセージのみに適用することができます。 メッセージストアプロバイダーとトランスポートプロバイダーは、どちらも受信者プロパティを設定できます。 
  
各受信者は、メッセージの送信の準備ができたときに、プロパティの値の配列にプロパティのコアセットを持つ必要があります。 必要な受信者プロパティのセットは次のとおりです。
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
これらのプロパティは、受信者へのアクセス、メッセージの送信、および他のユーザーとの比較に使用されます。 これらのプロパティの一部は、すぐに使用できるようにする必要はありません。 このプロパティを割り当てるには、名前解決プロセスに依存して、エントリ id を知らなくても受信者を最初に追加できます。 メッセージを送信する前に、ある時点で、 [IAddrBook:: ResolveName](iaddrbook-resolvename.md)を呼び出して、受信者一覧のすべての受信者が解決されるようにします。 詳細については、「[受信者名の解決](resolving-a-recipient-name.md)」を参照してください。
  
受信者リストは、アドレス帳コンテナー内のメッセージングユーザーまたは配布リストのエントリから、または1回から作成できます。 1回限りの受信者は、1つのメッセージのアドレス指定にのみ使用される一時エントリ、または個人用アドレス帳に追加されるエントリとして作成される受信者です。 1回限りのエントリ id とアドレスの形式は、MAPI によって定義されます。 これらの形式の詳細については、「 [1 回限りのアドレス](one-off-addresses.md)と[1 回限りのエントリ識別子](one-off-entry-identifiers.md)」を参照してください。
  
ユーザーが受信者リストを作成できるようにすることができます。
  
- アドレス帳のエントリのみを使用します。
    
- 1回限りのエントリのみを使用します。
    
- アドレス帳の受信者と1回の組み合わせの組み合わせ。
    
 **[共通アドレス] ダイアログボックスを使用して受信者リストを作成するには**
  
1. [ADRPARM](adrparm.md)構造体と[adrlist](adrlist.md)構造体へのポインターを割り当てます。 
    
2. **ADRPARM**構造体のメモリをゼロにし、 **adrlist**ポインターを NULL に設定します。 
    
3. [IAddrBook:: address](iaddrbook-address.md)を呼び出して、[アドレス] ダイアログボックスを表示し、 **ADRPARM**構造を設定します。 
    
4. [IMessage:: modifyrecipients](imessage-modifyrecipients.md)を呼び出し、 **adrlist**ポインターを渡します。 この構造体には、ユーザーによって選択された各受信者のプロパティが含まれます。 
    
 **プログラムで受信者リストを作成するには**
  
1. リストに含める受信者ごとに1つの[adrlist](adrentry.md)構造を含む**adrlist**構造を割り当てます。 各**adrentry**構造を、必要なプロパティと**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) を保持するために十分な大きさにします。
    
2. 各受信者について、 **adrlist**構造の**aentries**メンバーにプロパティ値の配列を設定します。 
    
3. MODRECIP_ADD フラグが設定されている[IMessage:: modifyrecipients](imessage-modifyrecipients.md)を呼び出します。 
    

