---
title: 未配信メッセージの再送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328680"
---
# <a name="resending-an-undelivered-message"></a>未配信メッセージの再送信
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信したメッセージを正常に配信できない場合、トランスポートプロバイダーは配信不能レポート (NDR) を送信します。 ユーザーがこれらの未配信メッセージの再送信を試みることができるかどうかは、クライアントによって設定されます。 メッセージの再送信をサポートする場合は、MAPI で提供されたフォームを使用するか、または独自のフォームを実装できます。 MAPI フォームには、失敗した受信者の名前と、可能であれば配信エラーの理由が表示され、ユーザーがメッセージを再送信できるようにするボタンが含まれています。
  
再送信メッセージを受信すると、元のメッセージとまったく同じように表示されます。 受信者は、送信時に最初に配信されたメッセージとその後の試行で区別できないようにする必要があります。 このメッセージの返信は、メッセージが最初に正常に送信された場合とまったく同じように動作します。
  
### <a name="to-resend-an-undelivered-message"></a>未配信のメッセージを再送信するには
  
1. [imapifolder:: CreateMessage](imapifolder-createmessage.md)を呼び出して、新しいメッセージを作成します。 
    
2. * * PR_MESSAGE_RECIPIENTS * * ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティ、 **PR_SENDER** 、 **PR_SENT_REPRESENTING**の各プロパティを除く、元のメッセージのすべてのプロパティをコピーします。 次のプロパティを変更してください。 
    
   - **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) を report の * * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) プロパティに設定します。
    
   - **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティで MSGFLAG_RESEND フラグを設定します。
    
   - 元のメッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティに、 **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) を設定します。
    
   - 各受信者について、 **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティで MAPI_SUBMITTED を設定します。 
    
   - 失敗した受信者ごとに複製します。 複製された受信者の**PR_RECIPIENT_TYPE**プロパティを MAPI_P1 に変更します。 そのため、失敗した受信者ごとに、受信者テーブルに2つのエントリがあります。1つは、 **PR_RECIPIENT_TYPE**が元の値に設定され、もう一方が**PR_RECIPIENT_TYPE**が MAPI_P1 に設定されている場合です。 
    
3. 必要に応じて、 [ScCreateConversationIndex](sccreateconversationindex.md)を呼び出して会話追跡を設定します。 
    
4. 新しいメッセージの[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出して、受信者リストを更新します。 
    
5. [IMessage:: submitmessage](imessage-submitmessage.md)を呼び出して、新しいメッセージを保存して送信します。 
    

