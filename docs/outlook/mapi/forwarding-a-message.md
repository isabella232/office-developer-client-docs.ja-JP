---
title: メッセージを転送
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 146c8b4d711982118fd9da185a5b095a1bae6b2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800113"
---
# <a name="forwarding-a-message"></a>メッセージを転送

**適用対象**: Outlook 
  
元のメッセージを送信すると同じタスクの多くは、メッセージを転送します。 まず、既定のメッセージ ストアと、送信トレイでは通常、送信されるメッセージを保持するために指定されているフォルダーを開くしを転送するメッセージを作成するのには、このフォルダーの[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出す必要があります。 受信トレイでは通常、元のメッセージを保持しているフォルダーを開く必要があります。 別のフォルダーを開く方法については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。
  
転送するメッセージを作成し、元の作成の主な違いでは、転送されたメッセージを表示して、プロパティのほとんどはに基づいてまたは元のメッセージのプロパティから直接コピーします。 
  
**メッセージを転送するには**
  
1. 既定のメッセージ ストアを開きます。 詳細については、[既定のメッセージ ストアを開く](opening-the-default-message-store.md)を参照してください。
    
2. [送信トレイ] フォルダーを開きます。 詳細については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。
    
3. 新しい転送されたメッセージを作成するのには、[送信トレイ] の[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 
    
4. 転送メッセージに次のプロパティをコピーするのには、元のメッセージの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。 
    
   - **PR\_本文**([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) は、リッチ テキスト形式、テキスト形式または HTML をサポートするかどうかによって異なります。
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティをコピーするのには、元のメッセージの**IMAPIProp::CopyTo**メソッドを呼び出すか、次を呼び出すことによって、元のメッセージからメッセージの添付ファイルをコピーします。各添付ファイルをコピーするための手順を次の 3 つのステップ:
    
   1. 新しい転送の新しい添付ファイルを作成するのには、メッセージの[IMessage::CreateAttach](imessage-createattach.md)メソッドを呼び出します。 
      
   2. コピーする添付ファイルを開くには元のメッセージの[IMessage::OpenAttach](imessage-openattach.md)メソッドを呼び出します。 
      
   3. 新しいものに古い添付ファイルからすべての添付ファイルのプロパティをコピーするのには、元のメッセージの**IMAPIProp::CopyTo**メソッドを呼び出します。 
    
6. **IMAPIProp::CopyTo**を呼び出すには次のプロパティは含まれません。 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING**プロパティ  <br/> |
|**PR_READ_RECEIPT_ENTRYID**([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY**プロパティ  <br/> |**PR_REPLY_RECIPIENT**プロパティ  <br/> |
|**PR_REPORT_ENTRYID**([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER**プロパティ  <br/> |
|**PR_SENT_REPRESENTING**プロパティ  <br/> |**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. インデントされ、元の送信者を含むヘッダーの段落を追加することによってメッセージのテキストを書式設定の転送、件名、および受信者の一覧の日付。 コンテンツとインターネット スタイルの先頭の文字を含めないでください。
    
2. [ScCreateConversationIndex](sccreateconversationindex.md)、元のメッセージの**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) のプロパティの値を渡してを呼び出します。
    
3. 転送メッセージのプレフィックスを設定します。 標準を使用している場合"FW:"、 **PR_NORMALIZED_SUBJECT**の先頭にこれらの文字を連結し、この新しい文字列に**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) を設定します。 **されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) を設定することはしません。 3 文字より長い文字列などの非標準のプレフィックスを使用している場合は、**されて**に格納します。 
    
4. **PR_RCVD_REPRESENTING**プロパティに対応する値には、 **PR_SENT_REPRESENTING**プロパティを設定します。 
    
5. 受信者リストを作成します。 詳細については、[受信者リストを作成する](creating-a-recipient-list.md)を参照してください。
    
6. または保存し、送信する[IMessage::SubmitMessage](imessage-submitmessage.md)を保存するのには、転送されたメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
## <a name="see-also"></a>関連項目

- [PidTagMessageAttachments 標準プロパティ](pidtagmessageattachments-canonical-property.md)

