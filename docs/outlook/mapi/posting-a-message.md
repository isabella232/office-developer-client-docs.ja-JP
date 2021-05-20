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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429769"
---
# <a name="posting-a-message"></a>メッセージの投稿

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの投稿は、メッセージの送信に似ています。 主な違いは宛先です。 1 つ以上のメッセージング システムで 1 つ以上の受信者に送信されるのではなく、投稿されたメッセージは現在のメッセージ ストア内のフォルダーに残ります。
  
### <a name="to-post-a-message"></a>メッセージを投稿するには
  
1. [IMsgStore::OpenEntry を呼び出して、移動先フォルダーを開きます](imsgstore-openentry.md)。 宛先フォルダーが受信トレイの場合は [、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出して **OpenEntry** に渡すエントリ識別子を探します。 
    
2. [IMAPIFolder::CreateMessage を呼び出して](imapifolder-createmessage.md)メッセージを作成します。 
    
3. メッセージの [IMAPIProp::SetProps メソッドを呼び出して設定](imapiprop-setprops.md) します。 
    
   - MSGFLAG_READ **PidTagMessageFlags** [(](pidtagmessageflags-canonical-property.md)PR_MESSAGE_FLAGS ) プロパティPR_MESSAGE_FLAGSフラグです。
    
   - プロパティ **PR_SENDER** します。 
    
   - プロパティ **PR_SENT_REPRESENTING** します。 
    
   - プロパティ **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) プロパティです。
    
   - プロパティ **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または PR_BODY **(** [PidTagBody](pidtagbody-canonical-property.md)) プロパティを指定します。
    
   - プロパティ **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティです。
    
   - プロパティ **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティです。
    
   - メッセージ クラスで必要なプロパティ。
    
4. メッセージを保存するには、 [メッセージの IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出します。 
    
5. 必要に応じて、添付ファイルを作成し、そのプロパティを設定し、保存します。 メッセージへの添付ファイルの追加の詳細については、「メッセージ添付ファイルの [作成」を参照してください](creating-a-message-attachment.md)。
    
6. **IMessage::SaveChanges を呼び出して** メッセージを保存します。 この時点で、移動先フォルダーのコンテンツ テーブルに表示されます。 
    
受信者リストを作成しない場合に注意してください。 代わりに、送信メッセージに対してトランスポート プロバイダーによって通常設定されるいくつかのプロパティを設定します。 
  
メッセージを表示フォルダーのコンテンツ テーブルに表示する前に断続的に保存する場合は、IPM サブツリーのルート フォルダーなどの非表示フォルダーにメッセージを作成し、ターゲット フォルダーに移動します。 
  

