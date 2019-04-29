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
  
メッセージを転送すると、元のメッセージを送信するのと同じタスクが多く行われます。 最初に、既定のメッセージストアと、送信メッセージ (通常は送信トレイ) を保持するように指定されているフォルダーを開き、転送するメッセージを作成するために、このフォルダーの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 また、元のメッセージを保持するフォルダー (通常は受信トレイ) も開く必要があります。 別のフォルダーを開く方法については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。
  
転送されるメッセージを作成し、元のメッセージを作成することの主な違いは、転送されたメッセージでは、ほとんどのプロパティが元のメッセージのプロパティから直接またはコピーされるかのどちらかです。 
  
**メッセージを転送するには**
  
1. 既定のメッセージストアを開きます。 詳細については、「[既定のメッセージストアを開く](opening-the-default-message-store.md)」を参照してください。
    
2. [送信トレイ] フォルダーを開きます。 詳細については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。
    
3. 送信トレイの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出して、新しい転送メッセージを作成します。 
    
4. 元のメッセージの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、次のプロパティを転送されたメッセージにコピーします。 
    
   - **\_** リッチテキスト形式、プレーンテキスト、または HTML をサポートしているかどうかに応じて、pr 本文 ([PidTagBody](pidtagbody-canonical-property.md))、 **pr\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) を使用します。
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティをコピーするか、または次のように呼び出して、元の message の**imapiprop:: CopyTo**メソッドを呼び出して、メッセージの添付ファイルを元のメッセージからコピーします。コピーする添付ファイルごとに、次の3つの手順を実行します。
    
   1. 新しい転送メッセージの[IMessage:: createattach](imessage-createattach.md)メソッドを呼び出して、新しい添付ファイルを作成します。 
      
   2. 元のメッセージの[IMessage:: openattach](imessage-openattach.md)メソッドを呼び出して、コピーする添付ファイルを開きます。 
      
   3. 元のメッセージの**imapiprop:: CopyTo**メソッドを呼び出して、すべての添付ファイルプロパティを古い添付ファイルから新しい添付ファイルにコピーします。 
    
6. **imapiprop:: CopyTo**に対する呼び出しには、次のプロパティを含めないでください。 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING**プロパティ  <br/> |
|**PR_READ_RECEIPT_ENTRYID**([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY**プロパティ  <br/> |**PR_REPLY_RECIPIENT**プロパティ  <br/> |
|**PR_REPORT_ENTRYID**([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER**プロパティ  <br/> |
|**PR_SENT_REPRESENTING**プロパティ  <br/> |**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. メッセージテキストの書式を設定するインデントと、元の送信者、送信日、件名、および受信者リストを含むヘッダー段落を追加します。 コンテンツにインターネットスタイルのプレフィックス文字を含めないでください。
    
2. [ScCreateConversationIndex](sccreateconversationindex.md)を呼び出し、元のメッセージの**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティの値を渡します。
    
3. 転送されるメッセージのプレフィックスを設定します。 標準の "FW:" を使用している場合は、これらの文字を**PR_NORMALIZED_SUBJECT**の先頭に連結し、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) をこの新しい文字列に設定します。 **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) を設定しません。 3文字を超える文字列など、標準的ではないプリフィックスを使用している場合は、 **PR_SUBJECT_PREFIX**に格納します。 
    
4. **PR_SENT_REPRESENTING**プロパティを**PR_RCVD_REPRESENTING**プロパティの対応する値に設定します。 
    
5. 受信者リストを作成します。 詳細については、「[受信者リストを作成](creating-a-recipient-list.md)する」を参照してください。
    
6. 転送されたメッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して保存します。また、 [IMessage:: submitmessage](imessage-submitmessage.md)に保存して送信します。 
    
## <a name="see-also"></a>関連項目

- [PidTagMessageAttachments 標準プロパティ](pidtagmessageattachments-canonical-property.md)

