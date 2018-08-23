---
title: 受信者テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803722"
---
# <a name="recipient-tables"></a>受信者テーブル

  
  
**適用対象**: Outlook 
  
受信者テーブルには、メッセージのすべての受信者に関する情報が含まれています。 メッセージ ストア プロバイダーは、受信者テーブルを実装し、クライアント アプリケーションが使用します。 クライアントは、 [IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出すことによって受信者テーブルにアクセスまたは場合は、メッセージ ・ ストア プロバイダーでサポートされている、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドにします。 インターフェイス識別子のプロパティ タグと IID_IMAPITable の**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) を指定することによって**OpenProperty**を持つ受信者テーブルをクライアントにアクセスします。 受信者テーブルへの変更は、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって可能です。 
  
受信者テーブルには、メッセージが送信されたかどうかに応じて、設定の異なる列があります。 次のプロパティは、受信者テーブルの設定の必要な列を構成します。
  
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md))
    
省略可能なプロパティは次のとおりです。
  
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS**([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
送信されたメッセージは、必要な列のセットに追加したプロパティを含める必要があります。
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
プロバイダーの実装では、によって、テーブルの[エントリ ID](entryid.md)、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) などの追加の列があります。
  
メッセージの送信をサポートする任意のメッセージ ストア プロバイダー、プロバイダーの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティに設定されている STORE_SUBMIT_OK ビットによって示されるなどの特定のセットのサポートを提供する必要があります受信者テーブルの実装で制限します。 ****、**または**、次のように存在して、プロパティの制限は、受信者テーブルのユーザーが使用可能にする必要がある制限の種類。 のみ、等しいと等しくない演算子は、プロパティの制限をサポートする必要があります。 これらの制限は、次のプロパティを操作する必要があります。
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **れない**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

