---
title: 送信メッセージの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342806"
---
# <a name="handling-an-outgoing-message"></a>送信メッセージの処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メッセージは、1つまたは複数のメッセージングシステムで1人または複数の受信者に送信されるメッセージ、またはメッセージストア内のフォルダーに投稿されるメッセージです。
  
## <a name="create-and-send-an-outgoing-message"></a>送信メッセージを作成および送信する
  
1. 既定のメッセージストアを開きます。 詳細については、「[メッセージストアを開く](opening-a-message-store.md)」および「[既定のメッセージストアを開く](opening-the-default-message-store.md)」を参照してください。
    
2. [送信トレイ] フォルダーを開きます。 詳細については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。
    
3. 送信トレイフォルダーの**imapifolder:: CreateMessage**メソッドを呼び出して、新しいメッセージを作成します。 詳細については、「 [imapifolder:: CreateMessage](imapifolder-createmessage.md)」を参照してください。
    
4. 1つまたは複数の解決された受信者を含む受信者リストを作成します。 詳細については、「[受信者リストを作成](creating-a-recipient-list.md)する」を参照してください。
    
5. 必要に応じて、件名を追加します。 詳細については、「[メッセージの件名の作成](creating-a-message-subject.md)」を参照してください。
    
6. メッセージテキストを追加します。 詳細については、「[メッセージテキストを作成する](creating-message-text.md)」を参照してください。
    
7. メッセージテキストが書式設定されている場合は、レンダリング情報を追加します。 詳細については、「[レンダリング情報を書式設定されたテキストに追加する](adding-rendering-information-to-formatted-text.md)」を参照してください。
    
8. 必要に応じて、1つまたは複数の添付ファイルを追加します。 詳細については、「[メッセージの添付ファイルを作成](creating-a-message-attachment.md)する」を参照してください。
    
9. 必要に応じて他のメッセージプロパティを設定し、 **IMessage:: submitmessage**を呼び出してメッセージを保存して送信します。 詳細については、「 [IMessage:: submitmessage](imessage-submitmessage.md)」を参照してください。
    
10. **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、送信されたメッセージを削除するか、または**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティで指定されたフォルダーに移動します。 詳細については、「[送信済みメッセージの処理](processing-a-sent-message.md)」を参照してください。
    
メッセージを送信する前に intermittantly 保存する場合は、メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 詳細については、「[メッセージを保存する](saving-a-message.md)」または「[メッセージを送信](sending-a-message.md)する」を参照してください。 
  
## <a name="in-this-section"></a>このセクションの内容

- [受信者リストを作成](creating-a-recipient-list.md)する: 受信者リストを作成する方法について説明します。
    
- [メッセージの件名の作成](creating-a-message-subject.md): メッセージの任意の件名を作成する方法について説明します。
    
- [メッセージテキストの作成](creating-message-text.md): メッセージテキストを作成する方法について説明します。
    
- [書式設定されたテキストへのレンダリング情報の追加](adding-rendering-information-to-formatted-text.md): 書式付きテキストのどこで添付ファイルがレンダリングされるかについて説明します。
    
- [メッセージ添付ファイルの](creating-a-message-attachment.md)作成: 添付ファイルを作成する方法について説明します。
    
- [メッセージを保存](saving-a-message.md)する: クライアントがメッセージを保存する方法について説明します。
    
- [メッセージの送信](sending-a-message.md): メッセージを送信する方法について説明します。
    
- [送信済みメッセージの処理](processing-a-sent-message.md): 送信メッセージを処理する方法を説明します。
    

