---
title: 送信メッセージを処理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ab293ee3813d77c3a954e8364736a89bc2330feb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800171"
---
# <a name="handling-an-outgoing-message"></a>送信メッセージを処理します。

**適用対象**: Outlook 
  
送信メッセージは、1 つまたは複数のメッセージング システム間で 1 つまたは複数の受信者に送信することができますか、メッセージ ・ ストア内のフォルダーに投稿するメッセージです。
  
## <a name="create-and-send-an-outgoing-message"></a>作成し、送信メッセージを送信します。
  
1. 既定のメッセージ ストアを開きます。 詳細については、[メッセージ ストアを開く](opening-a-message-store.md)と、[既定のメッセージ ストアを開く](opening-the-default-message-store.md)を参照してください。
    
2. [送信トレイ] フォルダーを開きます。 詳細については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。
    
3. 新しいメッセージを作成するのには、[送信トレイ] フォルダーの**IMAPIFolder::CreateMessage**メソッドを呼び出します。 詳細については、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を参照してください。
    
4. 解決された 1 つまたは複数の受信者と受信者のリストを作成します。 詳細については、[受信者リストを作成する](creating-a-recipient-list.md)を参照してください。
    
5. 必要に応じて、件名を追加します。 詳細については、[メッセージの件名を作成する](creating-a-message-subject.md)を参照してください。
    
6. メッセージ テキストを追加します。 詳細については、[メッセージ テキストの作成](creating-message-text.md)を参照してください。
    
7. メッセージのテキストがフォーマットされている場合は、レンダリング情報を追加します。 詳細については、[テキストの書式設定にレンダリング情報の追加](adding-rendering-information-to-formatted-text.md)を参照してください。
    
8. 必要に応じて、1 つまたは複数の添付ファイルを追加します。 詳細については、[メッセージの添付ファイルを作成する](creating-a-message-attachment.md)を参照してください。
    
9. 必要に応じてその他のメッセージのプロパティを設定し、保存して**IMessage::SubmitMessage**を呼び出すことによって、メッセージを送信します。 詳細については、 [IMessage::SubmitMessage](imessage-submitmessage.md)を参照してください。
    
10. 場合に送信されるメッセージを削除します**PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE または特定のフォルダーに移動する**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティで。 詳細については、[送信メッセージの処理](processing-a-sent-message.md)を参照してください。
    
Intermittantly したい場合は、メッセージを送信する前に保存、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 詳細についてを参照してください、[メッセージを保存](saving-a-message.md)または[メッセージを送信](sending-a-message.md)します。 
  
## <a name="in-this-section"></a>このセクションの内容

- [受信者リストを作成する](creating-a-recipient-list.md): 受信者のリストを作成する方法について説明します。
    
- [メッセージの件名を作成する](creating-a-message-subject.md): メッセージの任意の件名を作成する方法について説明します。
    
- [メッセージ テキストを作成する](creating-message-text.md): メッセージのテキストを作成する方法について説明します。
    
- [形式のテキストをレンダリング情報を追加する](adding-rendering-information-to-formatted-text.md): 書式設定されたテキストの添付ファイルが表示されるについて説明します。
    
- [メッセージの添付ファイルを作成する](creating-a-message-attachment.md): 添付ファイルを作成する方法について説明します。
    
- [メッセージを保存する](saving-a-message.md): クライアントがメッセージを保存する方法について説明します。
    
- [メッセージの送信](sending-a-message.md): メッセージを送信する方法について説明します。
    
- [送信メッセージの処理](processing-a-sent-message.md): メッセージを処理することができますを送信する方法について説明します。
    

