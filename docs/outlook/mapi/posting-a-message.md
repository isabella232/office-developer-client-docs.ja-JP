---
title: メッセージを投稿
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 33bf6780979ee25739abf93d89744e1517363c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803692"
---
# <a name="posting-a-message"></a>メッセージを投稿

**適用されます**: Outlook 
  
メッセージを投稿することは、メッセージを送信することに似ています。 主な違いは、リンク先です。 1 つまたは複数のメッセージング システム間で 1 つまたは複数の受信者に送信されるのではなく、現在のメッセージ ストア内のフォルダーに投稿されたメッセージのままです。
  
### <a name="to-post-a-message"></a>メッセージを投稿するには
  
1. [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出すことによって、コピー先のフォルダーを開きます。 コピー先のフォルダーが受信トレイの場合は、 [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出すことによって**OpenEntry**に渡すためのエントリ id を検索します。 
    
2. メッセージを作成するのには[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を呼び出します。 
    
3. メソッドを呼び出してメッセージの[IMAPIProp::SetProps](imapiprop-setprops.md)を設定します。 
    
   - **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) のプロパティに MSGFLAG_READ フラグです。
    
   - **PR_SENDER**プロパティです。 
    
   - **PR_SENT_REPRESENTING**プロパティです。 
    
   - **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) のプロパティです。
    
   - **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティです。
    
   - **あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) のプロパティです。
    
   - **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティです。
    
   - メッセージ クラスに必要なプロパティです。
    
4. メッセージを保存するのには、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
5. 必要に応じて、添付ファイルを作成、そのプロパティを設定し、保存します。 メッセージに添付ファイルを追加する方法の詳細については、[メッセージの添付ファイルを作成する](creating-a-message-attachment.md)を参照してください。
    
6. メッセージを保存するのには**IMessage::SaveChanges**を呼び出します。 この時点でコピー先のフォルダーの内容のテーブルに表示されます。 
    
受信者リストを作成しないことに注意してください。 代わりに、送信されたメッセージのトランスポート プロバイダーが正常に設定されているいくつかのプロパティを設定します。 
  
断続的にする前に表示されているフォルダーの内容のテーブルに表示されるメッセージを保存する場合は、IPM サブツリーのルート フォルダーなどの非表示のフォルダーの代わりに作成し、ターゲット フォルダーに移動します。 
  

