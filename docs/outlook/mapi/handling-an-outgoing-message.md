---
title: 送信メッセージの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 18fe188f7906b3a2fdd8192a353cc8ba39ad0247
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556694"
---
# <a name="handling-an-outgoing-message"></a>送信メッセージの処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メッセージとは、1 つ以上のメッセージング システムで 1 つ以上の受信者に送信したり、メッセージ ストア内のフォルダーに投稿したりできるメッセージです。
  
## <a name="create-and-send-an-outgoing-message"></a>送信メッセージの作成と送信
  
1. 既定のメッセージ ストアを開きます。 詳細については、「メッセージ ストアを [開く」および「](opening-a-message-store.md) 既定 [のメッセージ ストアを開く」を参照してください](opening-the-default-message-store.md)。
    
2. [送信ボックス] フォルダーを開きます。 詳細については、「メッセージ ストア フォルダー [を開く」を参照してください](opening-a-message-store-folder.md)。
    
3. Outbox フォルダーの **IMAPIFolder::CreateMessage** メソッドを呼び出して、新しいメッセージを作成します。 詳細については [、「IMAPIFolder::CreateMessage 」 を参照してください](imapifolder-createmessage.md)。
    
4. 1 つ以上の解決済み受信者を含む受信者リストを作成します。 詳細については、「受信者リストの [作成」を参照してください](creating-a-recipient-list.md)。
    
5. 必要に応じて、件名を追加します。 詳細については、「メッセージサブジェクトの [作成」を参照してください](creating-a-message-subject.md)。
    
6. メッセージ テキストを追加します。 詳細については、「メッセージ テキストの作成 [」を参照してください](creating-message-text.md)。
    
7. メッセージ テキストが書式設定されている場合は、レンダリング情報を追加します。 詳細については、「書式設定されたテキスト [にレンダリング情報を追加する」を参照してください](adding-rendering-information-to-formatted-text.md)。
    
8. 必要に応じて、1 つ以上の添付ファイルを追加します。 詳細については、「メッセージ添付ファイルの [作成」を参照してください](creating-a-message-attachment.md)。
    
9. 必要に応じて他のメッセージ プロパティを設定し **、IMessage::SubmitMessage** を呼び出してメッセージを保存して送信します。 詳細については [、「IMessage::SubmitMessage」を参照してください](imessage-submitmessage.md)。
    
10. **PR \_ DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、送信されたメッセージを削除するか **、PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティで識別されるフォルダーに移動します。 詳細については、「送信されたメッセージ [の処理」を参照してください](processing-a-sent-message.md)。
    
メッセージを送信する前にメッセージを相互に保存する場合は、メッセージの [IMAPIProp::SaveChanges メソッドを呼び出](imapiprop-savechanges.md) します。 詳細については、「メッセージの保存[」または「メッセージの](saving-a-message.md)[送信」を参照してください](sending-a-message.md)。 
  
## <a name="in-this-section"></a>このセクションの内容

- [受信者リストの作成](creating-a-recipient-list.md): 受信者リストを作成する方法について説明します。
    
- [メッセージ件名の作成](creating-a-message-subject.md): メッセージのオプションの件名を作成する方法について説明します。
    
- [メッセージ テキストの作成](creating-message-text.md): メッセージ テキストを作成する方法について説明します。
    
- [書式設定されたテキストにレンダリング情報を](adding-rendering-information-to-formatted-text.md)追加する : 書式設定されたテキスト内で添付ファイルをレンダリングする場所について説明します。
    
- [メッセージ添付ファイルの作成](creating-a-message-attachment.md): 添付ファイルを作成する方法について説明します。
    
- [メッセージの保存](saving-a-message.md): クライアントがメッセージを保存する方法について説明します。
    
- [メッセージの送信 :](sending-a-message.md)メッセージを送信する方法について説明します。
    
- [送信メッセージの処理](processing-a-sent-message.md): 送信メッセージを処理する方法について説明します。
    

