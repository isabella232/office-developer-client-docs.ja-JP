---
title: 受信者テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fc71a5128796d74f06a896ad8b1bc2cdc153c060
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599152"
---
# <a name="recipient-tables"></a>受信者テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者テーブルには、メッセージのすべての受信者に関する情報が含まれる。 メッセージ ストア プロバイダーは受信者テーブルを実装し、クライアント アプリケーションはそれらを使用します。 [クライアントは、IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出して受信者テーブルにアクセスするか、メッセージ ストア プロバイダーがそれをサポートしている場合は[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドにアクセスします。 クライアントは、プロパティ タグに **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) を指定し、インターフェイス識別子に IID_IMAPITable を指定して **、OpenProperty** を使用して受信者テーブルにアクセスします。 受信者テーブルに対する変更は [、IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを呼び出すことによって行えます。 
  
受信者テーブルの列セットは、メッセージが送信されたかどうかによって異なります。 次のプロパティは、受信者テーブルで必要な列セットを構成します。
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
オプションのプロパティは次のとおりです。
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
送信されたメッセージには、次の追加プロパティを必須の列セットに含める必要があります。
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
プロバイダーの実装によっては、PR_SENDER_NAME **(** [PidTagSenderName](pidtagsendername-canonical-property.md)) や [ENTRYID](entryid.md)などの追加の列が表に含まれます。
  
プロバイダー **の PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)プロパティで設定されている STORE_SUBMIT_OK ビットによって示されるメッセージ送信をサポートするメッセージ ストア プロバイダーは、受信者テーブルの実装における特定の制限セットをサポートする必要があります。 **AND** **、OR、** およびプロパティの制限は、受信者テーブルのユーザーが使用できる制限の種類の中にあります。 プロパティの制限では、等しい演算子と等しくない演算子のみをサポートする必要があります。 これらの制限は、次のプロパティで動作する必要があります。
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

