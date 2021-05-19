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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432668"
---
# <a name="resending-an-undelivered-message"></a>未配信メッセージの再送信
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーは、送信したメッセージを正常に配信できない場合に配信不可レポート (NDR) を送信します。 ユーザーがこれらの未配信メッセージの再送信を試みるかどうかは、クライアントの判断です。 メッセージの再送信をサポートする場合は、MAPI によって提供されるフォームを使用するか、独自のフォームを実装できます。 MAPI フォームには、失敗した受信者の名前と配信エラーの理由 (可能な場合) が表示され、選択するとユーザーがメッセージを再送信できるボタンが含まれます。
  
再送信メッセージを受信すると、元のメッセージとまったく同じに見える必要があります。 受信者は、送信時の最初の試みで配信されたメッセージと、それ以降の試行を区別できない必要があります。 このメッセージの返信は、メッセージが最初に正常に送信された場合とまったく同じ動作をする必要があります。
  
### <a name="to-resend-an-undelivered-message"></a>配信されていないメッセージを再送信するには
  
1. [IMAPIFolder::CreateMessage を呼び出して](imapifolder-createmessage.md)新しいメッセージを作成します。 
    
2. ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティ、および PR_SENDER プロパティと PR_SENT_REPRESENTING プロパティを除く、元 **のメッセージからすべての** プロパティ **をコピー** します。 次のプロパティを変更します。 
    
   - **[PR_MESSAGE_CLASS** ] ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) をレポートの **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) プロパティに設定します。
    
   - プロパティ ( MSGFLAG_RESEND [PidTagMessageFlags](pidtagmessageflags-canonical-property.md) **)** PR_MESSAGE_FLAGSフラグを設定します。
    
   - [PR_ORIGINAL_ENTRYID ] ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) を元のメッセージのプロパティ [(PidTagEntryId)](pidtagentryid-canonical-property.md)プロパティに **PR_ENTRYID設定します**。 
    
   - 各受信者に対して、MAPI_SUBMITTED ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) **PR_RECIPIENT_TYPE** プロパティに設定します。 
    
   - 失敗した各受信者を複製します。 重複する **受信者PR_RECIPIENT_TYPE** のプロパティを [削除] にMAPI_P1。 したがって、失敗した受信者ごとに、受信者テーブルに **2** つのエントリがあります。1 つは PR_RECIPIENT_TYPE が元の値に設定され、もう 1 つは PR_RECIPIENT_TYPE が **MAPI_P1** に設定されています。 
    
3. [必要に応じて、ScCreateConversationIndex](sccreateconversationindex.md)を呼び出して会話の追跡を設定します。 
    
4. 新しいメッセージの [IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを呼び出して、受信者リストを更新します。 
    
5. [IMessage::SubmitMessage を呼び出](imessage-submitmessage.md)して、新しいメッセージを保存して送信します。 
    

