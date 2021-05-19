---
title: メッセージの転送
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433179"
---
# <a name="forwarding-a-message"></a>メッセージの転送

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの転送には、元のメッセージの送信と同じタスクの多くが含まれます。 最初に、既定のメッセージ ストアと、送信メッセージを保持するために指定されているフォルダー (通常は送信ボックス) を開き、このフォルダーの [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、転送するメッセージを作成する必要があります。 また、元のメッセージを保持するフォルダー (通常は受信トレイ) を開く必要があります。 異なるフォルダーを開く方法については、「 [メッセージ ストア フォルダーを開く」を参照してください](opening-a-message-store-folder.md)。
  
転送するメッセージを作成し、元のメッセージを作成する主な違いは、転送されたメッセージでは、ほとんどのプロパティが元のメッセージのプロパティに基づくか、元のメッセージのプロパティから直接コピーされるという点です。 
  
**メッセージを転送するには**
  
1. 既定のメッセージ ストアを開きます。 詳細については、「既定のメッセージ [ストアを開く」を参照してください](opening-the-default-message-store.md)。
    
2. [送信ボックス] フォルダーを開きます。 詳細については、「メッセージ ストア フォルダー [を開く」を参照してください](opening-a-message-store-folder.md)。
    
3. Outbox の [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、新しい転送メッセージを作成します。 
    
4. 元のメッセージの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、転送されたメッセージに次のプロパティをコピーします。 
    
   - **PR \_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **、PR \_ HTML** [(PidTagHtml)、](pidtaghtml-canonical-property.md)または PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) は、リッチ テキスト形式、プレーン テキスト、または HTML をサポートするかどうかに応じて異なる。 
    
   - **PR \_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. 元のメッセージの **IMAPIProp::CopyTo** メソッドを呼び出して PR_MESSAGE_ATTACHMENTS ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティをコピーするか、コピーする添付ファイルごとに次の **3** つの手順を実行して、元のメッセージからメッセージ添付ファイルをコピーします。
    
   1. 新しい転送されたメッセージの [IMessage::CreateAttach](imessage-createattach.md) メソッドを呼び出して、新しい添付ファイルを作成します。 
      
   2. 元のメッセージの [IMessage::OpenAttach](imessage-openattach.md) メソッドを呼び出して、コピーする添付ファイルを開きます。 
      
   3. 元のメッセージの **IMAPIProp::CopyTo** メソッドを呼び出して、すべての添付ファイル プロパティを古い添付ファイルから新しい添付ファイルにコピーします。 
    
6. **IMAPIProp::CopyTo** への呼び出しには、次のプロパティを含めない。 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING** プロパティ  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY** プロパティ  <br/> |**PR_REPLY_RECIPIENT** プロパティ  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER** プロパティ  <br/> |
|**PR_SENT_REPRESENTING** プロパティ  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. インデントと、元の送信者、送信日、件名、受信者リストを含むヘッダー段落を追加して、メッセージ テキストの書式を設定します。 コンテンツにインターネット スタイルのプレフィックス文字を含めることはできません。
    
2. [ScCreateConversationIndex](sccreateconversationindex.md)を呼び出し、元のメッセージのプロパティ[(PidTagConversationIndex)](pidtagconversationindex-canonical-property.md)プロパティPR_CONVERSATION_INDEX値を渡します。
    
3. 転送されたメッセージのプレフィックスを設定します。 標準の "FW:" を使用している場合は、これらの文字を **PR_NORMALIZED_SUBJECT** の先頭に連結し **、PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) をこの新しい文字列に設定します。 [(PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md) **PR_SUBJECT_PREFIX設定** しない。 3 文字を超える文字列など、標準以外のプレフィックスを使用している場合は、そのプレフィックスを **PR_SUBJECT_PREFIX。** 
    
4. プロパティの **PR_SENT_REPRESENTING** プロパティに対応する **値を設定** PR_RCVD_REPRESENTINGします。 
    
5. 受信者リストを作成します。 詳細については、「受信者リストの [作成」を参照してください](creating-a-recipient-list.md)。
    
6. 転送されたメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出して保存するか [、IMessage::SubmitMessage](imessage-submitmessage.md) を呼び出して保存して送信します。 
    
## <a name="see-also"></a>関連項目

- [PidTagMessageAttachments 標準プロパティ](pidtagmessageattachments-canonical-property.md)

