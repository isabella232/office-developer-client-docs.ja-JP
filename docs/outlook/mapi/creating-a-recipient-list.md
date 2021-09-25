---
title: 受信者リストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e460765d57e4e40cc2739b39521b995c64ba5cf0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584669"
---
# <a name="creating-a-recipient-list"></a>受信者リストの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者リストは、メッセージの宛先である各メッセージ受信者のプロパティ値構造の配列を含む [ADRLIST](adrlist.md) 構造体です。 受信者は、人間のユーザー、コンピューター、またはフォルダーを表します。 送信するメッセージはすべて、名前解決プロセスを実行した少なくとも 1 人の受信者を必要とします **。つまり、PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが受信者のプロパティ値配列に含まれる必要があります。 
  
受信者のプロパティは、アドレス帳プロパティとメッセージ プロパティの組み合わせです。 受信者プロパティは、特定の受信者のすべてのメッセージに適用するか、現在のメッセージにのみ適用できます。 メッセージ ストアとトランスポート プロバイダーの両方で受信者のプロパティを設定できます。 
  
各受信者は、メッセージを送信する準備が整うまで、プロパティ値配列内のプロパティのコア セットを持っている必要があります。 必要な受信者プロパティのセットは次のとおりです。
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
これらのプロパティは、受信者にアクセスし、メッセージを送信し、他のユーザーと比較するために使用されます。 これらのプロパティのすべては、すぐ利用できる必要があります。 このプロパティを割り当てるには、名前解決プロセスに依存して、エントリ識別子を知らなくても、最初に受信者を追加できます。 メッセージを送信する前に [、IAddrBook::ResolveName](iaddrbook-resolvename.md) を呼び出して、受信者リスト内のすべての受信者が解決されるのを確認します。 詳細については、「受信者名の [解決」を参照してください](resolving-a-recipient-name.md)。
  
受信者リストは、メッセージング ユーザーまたはアドレス帳コンテナー内の配布リスト エントリ、または 1 回きりから作成できます。 1 回限りは、1 つのメッセージへのアドレス指定にのみ使用する一時的なエントリとして作成される受信者、または個人用アドレス帳に追加するエントリとして作成される受信者です。 1 回のエントリ識別子とアドレスの形式は、MAPI によって定義されます。 これらの形式の詳細については [、「One-Off Addresses and](one-off-addresses.md) [One-Off Entry IDENTIFIERs」を参照してください](one-off-entry-identifiers.md)。
  
ユーザーが受信者リストを作成できます。
  
- アドレス帳からのエントリがある場合のみ。
    
- 1 回限定のエントリの場合のみ。
    
- アドレス帳の受信者と 1 回きりを組み合わせて使用します。
    
 **[共通アドレス] ダイアログ ボックスを使用して受信者リストを作成するには**
  
1. [ADRPARM 構造体と ADRLIST](adrparm.md)構造体へのポインター[を割り当](adrlist.md)てる。 
    
2. **ADRPARM 構造体のメモリを 0 に** し **、ADRLIST** ポインターを NULL に設定します。 
    
3. [IAddrBook::Address を](iaddrbook-address.md)呼び出して、アドレス ダイアログ ボックスを表示し **、ADRPARM 構造を設定** します。 
    
4. [IMessage::ModifyRecipients を呼び出し](imessage-modifyrecipients.md)**、ADRLIST ポインターを渡** します。 この構造には、ユーザーが選択した各受信者のプロパティが含まれる。 
    
 **受信者リストをプログラムで作成するには**
  
1. リストに **含める受信者ごとに** [1 つの ADRENTRY](adrentry.md) 構造を含む ADRLIST 構造を割り当てる。 各 **ADRENTRY 構造を、** 必要なプロパティとプロパティ [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)を保持するのに十分な **PR_RECIPIENT_TYPE** してください。
    
2. 受信者ごとに **、ADRLIST** 構造体の **aEntries** メンバーのプロパティ値配列を設定します。 
    
3. [IMessage::ModifyRecipients](imessage-modifyrecipients.md)を呼び出し、MODRECIP_ADD設定します。 
    

