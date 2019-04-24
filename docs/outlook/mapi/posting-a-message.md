---
title: メッセージの投稿
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350751"
---
# <a name="posting-a-message"></a>メッセージの投稿

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを投稿することは、メッセージの送信と似ています。 主な違いは、宛先です。 1つまたは複数のメッセージングシステムで1人または複数の受信者に転送されるのではなく、現在のメッセージストア内のフォルダーに投稿されたメッセージが残っています。
  
### <a name="to-post-a-message"></a>メッセージを投稿するには
  
1. [IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、宛先フォルダーを開きます。 宛先フォルダーが受信トレイの場合は、 [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を呼び出して**openentry**に渡すエントリ識別子を見つけます。 
    
2. [imapifolder:: CreateMessage](imapifolder-createmessage.md)を呼び出して、メッセージを作成します。 
    
3. メッセージの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、次のように設定します。 
    
   - **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグ。
    
   - **PR_SENDER**プロパティ。 
    
   - **PR_SENT_REPRESENTING**プロパティ。 
    
   - **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) プロパティ。
    
   - **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ。
    
   - **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティ。
    
   - **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティ。
    
   - メッセージクラスに必要なすべてのプロパティ。
    
4. メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、メッセージを保存します。 
    
5. 必要に応じて、添付ファイルを作成し、そのプロパティを設定して保存します。 メッセージへの添付ファイルの追加の詳細については、「[メッセージの添付ファイルを作成](creating-a-message-attachment.md)する」を参照してください。
    
6. メッセージを保存するには、 **IMessage:: SaveChanges**を呼び出します。 この時点で、移動先フォルダーの contents テーブルに表示されます。 
    
受信者リストは作成されていないことに注意してください。 代わりに、送信されたメッセージのトランスポートプロバイダーによって設定されるプロパティをいくつか設定します。 
  
表示されているフォルダーの contents テーブルにメッセージを表示する前に、メッセージを保存する場合は、そのメッセージを IPM サブツリーのルートフォルダーなどの非表示のフォルダー内に作成して、移動先のフォルダーに移動します。 
  

