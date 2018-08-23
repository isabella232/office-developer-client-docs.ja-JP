---
title: 受信者リストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799878"
---
# <a name="creating-a-recipient-list"></a>受信者リストの作成

  
  
**適用対象**: Outlook 
  
受信者一覧は、各メッセージの受信者のプロパティの値の構造体の配列を含む[ADRLIST](adrlist.md)構造体など、メッセージの送信先。 受信者には、人間のユーザー、コンピューター、またはフォルダーを表すことができます。 すべてのメッセージを送信するには、名前解決プロセスを使用された 1 つ以上の受信者が必要とする、受信者のプロパティの値の配列で、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティが含まれていることを確認するプロセスです。 
  
受信者のプロパティは、アドレス帳のプロパティとメッセージのプロパティの組み合わせです。 受信者のプロパティは、特定の受信者のすべてのメッセージにするか、現在のメッセージにのみ適用できます。 両方のメッセージ ・ ストアと、トランスポート プロバイダーは、受信者のプロパティを設定できます。 
  
各受信者は、メッセージを送信する準備ができました時点でそのプロパティ値の配列にプロパティのコア セットが必要です。 受信者のプロパティのセットは次のとおりです。
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
受信者のアクセス、メッセージを送信して他のユーザーと比較するには、これらのプロパティが使用されます。 すべてのプロパティはすぐに使用できる必要があります。 できる受信者を追加する最初のエントリの識別子を知らなくてもこのプロパティを割り当てるには、名前解決の処理に依存すること。 メッセージを送信する前に、いくつかの時点ですべての受信者リストに受信者が解決するかどうかを確認するのには[IAddrBook::ResolveName](iaddrbook-resolvename.md)を呼び出します。 詳細については、[受信者名を解決する](resolving-a-recipient-name.md)を参照してください。
  
ユーザーまたは配布リストのエントリをアドレス帳コンテナー内のメッセージと、一時アドレスから、受信者の一覧を作成できます。 一時アドレスは、1 つのメッセージをアドレス指定のみに使用する一時的なエントリ、または個人用アドレス帳に追加するエントリとして作成される受信者です。 一時エントリ id とアドレスの形式は、MAPI によって定義されます。 これらの形式の詳細については、 [1 回限りのアドレス](one-off-addresses.md)と[1 回限りのエントリ Id](one-off-entry-identifiers.md)を参照してください。
  
ユーザーは、受信者のリストを作成するを有効にすることができます。
  
- でアドレス帳のエントリです。
    
- で 1 回限りのエントリです。
    
- アドレス帳の受信者と一時アドレスの組み合わせです。
    
 **共通のアドレス] ダイアログ ボックスを使用して受信者のリストを作成するには**
  
1. [ADRPARM](adrparm.md)構造体と、 [ADRLIST](adrlist.md)構造体へのポインターを割り当てます。 
    
2. **ADRPARM**構造体のメモリを 0 し、 **ADRLIST**のポインターを NULL に設定します。 
    
3. [アドレス] ダイアログ ボックスを表示し、 **ADRPARM**構造体を作成する[IAddrBook::Address](iaddrbook-address.md)を呼び出します。 
    
4. [IMessage::ModifyRecipients](imessage-modifyrecipients.md)、 **ADRLIST**ポインターを渡すことを呼び出します。 この構造体は、各ユーザーが選択されている受信者のプロパティに含まれます。 
    
 **受信者の一覧をプログラムで作成するには**
  
1. リストに含まれる受信者ごとの 1 つの[ADRENTRY](adrentry.md)構造体を含む**ADRLIST**構造体を割り当てます。 各**ADRENTRY**構造体の必要なプロパティ、および**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) を保持するのに十分な大きさを確認します。
    
2. 各受信者について、 **ADRLIST**構造体の**aEntries**メンバーのプロパティ値の配列を設定します。 
    
3. MODRECIP_ADD フラグを設定して[IMessage::ModifyRecipients](imessage-modifyrecipients.md)を呼び出します。 
    

