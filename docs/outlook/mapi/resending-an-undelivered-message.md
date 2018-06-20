---
title: メッセージの配信を再送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4fd0bf5a542e006ec743dbb7fe03d3331875c6d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803754"
---
# <a name="resending-an-undelivered-message"></a>メッセージの配信を再送信
  
**適用されます**: Outlook 
  
トランスポート プロバイダーは、送信したメッセージを正常に配信できない場合に、配信不能レポート (NDR) を送信します。 クライアントはユーザーがこれらの配信不能メッセージの再送を試みることができるかどうか。 サポートする場合、メッセージを再送信 MAPI によって提供されるフォームを使用してか、独自に実装します。 MAPI フォームが可能であれば、失敗した受信者と配信の失敗の理由の名前を表示し、ボタンが含まれていますが、選択すると、メッセージを再送信するユーザーに許可します。
  
再送信されたメッセージを受信すると、元のメッセージとまったく同じになります。 受信者は、転送の最初の試行は、またはそれ以降の試行で配信されたメッセージとを区別することことがあります。 このメッセージに返信は、メッセージが送信された正常に初めて場合とまったく同様に動作するはず。
  
### <a name="to-resend-an-undelivered-message"></a>メッセージの配信を再送信するには
  
1. 新しいメッセージを作成するのには[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を呼び出します。 
    
2. 元のメッセージからコピーするすべてのプロパティを除く、* * PR_MESSAGE_RECIPIENTS * * ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティ、および**PR_SENDER**と**PR_SENT_REPRESENTING**のプロパティです。 次のプロパティの変更を行います。 
    
   - **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) に、レポートの設定 * * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) のプロパティです。
    
   - **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティでは、MSGFLAG_RESEND フラグを設定します。
    
   - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを元のメッセージの**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) に設定します。
    
   - 各受信者について、 **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティに MAPI_SUBMITTED を設定します。 
    
   - 失敗した各受信者が重複してください。 重複した受信者の**PR_RECIPIENT_TYPE**プロパティを MAPI_P1 に変更します。 したがって、障害が発生した受信者ごとにエントリーがあるようになりました 2 受信者テーブルの: **PR_RECIPIENT_TYPE**で 1 つが元の値に設定し、MAPI_P1 に**PR_RECIPIENT_TYPE**と、その他の設定です。 
    
3. 会話が必要な場合にトラッキングを設定するのには[ScCreateConversationIndex](sccreateconversationindex.md)を呼び出します。 
    
4. 受信者の一覧を更新するための新しいメッセージの[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出します。 
    
5. 保存し、新しいメッセージを送信する[IMessage::SubmitMessage](imessage-submitmessage.md)を呼び出します。 
    

