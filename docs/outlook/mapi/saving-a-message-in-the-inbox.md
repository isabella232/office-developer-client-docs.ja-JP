---
title: 受信トレイへのメッセージの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e79133ed4928495dcf75b59877a82d3228773883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586285"
---
# <a name="saving-a-message-in-the-inbox"></a>受信トレイへのメッセージの保存

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **いずれかの受信者に受信トレイにメッセージを格納するには**
  
1. 受信トレイのエントリ id を取得するために[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出します。 
    
2. 受信トレイを開き、それへのポインターを取得する[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
    
3. メッセージを作成するのには、受信トレイの[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 
    
4. **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) と**あるの PR_SUBJECT** ([を追加するのには、メッセージの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すPidTagSubject](pidtagsubject-canonical-property.md)) のプロパティです。 
    
5. 各添付ファイルを作成、そのプロパティを設定し、それを保存します。 メッセージに添付ファイルを追加する方法の詳細については、[メッセージの添付ファイルを作成する](creating-a-message-attachment.md)を参照してください。
    
6. メッセージを保存するのには**IMessage::SaveChanges**を呼び出します。 この時点で、受信トレイの内容のテーブルに表示されます。 
    
メッセージ intermittantly を保存する前に、受信トレイの内容のテーブルに表示する場合は、IPM サブツリーのルート フォルダーなどの非表示のフォルダーの代わりに作成し、受信トレイに移動します。 
  

