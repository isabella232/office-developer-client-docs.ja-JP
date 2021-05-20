---
title: 返信の送信
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f47741369b1091c0dd24358e063de8f4675000fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437449"
---
# <a name="sending-a-reply"></a>返信の送信

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションは、通常、元のメッセージの送信者にのみ送信される返信と、送信者に加えて元のメッセージの受信者リストに含まれる他のすべての受信者に送信される応答の 2 種類をサポートします。 この 2 番目の種類の返信は、通常、すべてのメッセージの返信と呼ばれます。
  
いずれかの種類の返信を送信するには、元のメッセージを送信する場合と同じタスクの一部を実装します。 たとえば、既定のメッセージ ストアと送信メッセージ フォルダー (通常は送信ボックス) を開き、送信フォルダーの [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して返信を作成します。 また、元のメッセージを保持するフォルダー (通常は受信トレイ) を開きます。 異なるフォルダーを開く方法については、「 [メッセージ ストア フォルダーを開く」を参照してください](opening-a-message-store-folder.md)。
  
返信の作成と元のメッセージの作成の主な違いは、返信の場合、ほとんどのプロパティは元のメッセージのプロパティに基づくか、元のメッセージのプロパティから直接コピーされる点です。 添付ファイル - メッセージ **のPR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティは、特に除外されます。 返信のすべてのメッセージの受信者リストは **、PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey)](pidtagreceivedbysearchkey-canonical-property.md)プロパティで表される受信者と、すべてのブラインド カーボン コピー受信者が削除された元のメッセージの一覧から作成されます。 プロパティ **PR_RECEIVED_BY_SEARCH_KEY** 現在のユーザーを表します。 
  
### <a name="to-send-a-reply"></a>返信を送信する
  
1. 既定のメッセージ ストアを開きます。 詳細については、「既定のメッセージ [ストアを開く」を参照してください](opening-the-default-message-store.md)。
    
2. [送信ボックス] フォルダーを開きます。 詳細については、「メッセージ ストア フォルダー [を開く」を参照してください](opening-a-message-store-folder.md)。
    
3. 応答を作成するには [、Outbox の IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出します。 
    
4. 元のメッセージの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、次のプロパティを返信メッセージにコピーします。 
    
   - **PR \_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **または** PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) は、リッチ テキスト形式をサポートするかどうかに応じて異なる。
    
   - **PR \_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)を指定します。返信が受信者リスト全体に移動する場合。
    
   - **PR \_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))。
    
5. **IMAPIProp::CopyTo** への呼び出しには、次のプロパティを含めない。
    
    |||
    |:-----|:-----|
    |**PR \_ クライアント \_ の送信 \_ 時間** <br/> |**PR \_ メッセージ \_ の \_ 配信時間** <br/> |
    |**PR \_ メッセージ \_ のダウンロード \_ 時間** <br/> |**PR \_ メッセージ \_ フラグ** <br/> |
    |**PR \_ ORIGINATOR \_ DELIVERY \_ REPORT\REQUESTED** <br/> |**PR \_RCVD \_ REPRESENTING** プロパティ  <br/> |
    |**PR \_ READ \_ RECEIPT \_ ENTRYID** <br/> |**PR \_ 読み \_ 取り受信 \_ 確認要求** <br/> |
    |**PR \_RECEIVED \_ BY** プロパティ  <br/> |**PR \_REPLY \_ RECIPIENT** プロパティ  <br/> |
    |**PR \_ レポート \_ ENTRYID** <br/> |**PR \_SENDER** プロパティ  <br/> |
    |**PR \_SENT \_ REPRESENTING** プロパティ  <br/> |**PR \_ SENTMAIL \_ ENTRYID** <br/> |
    |**PR \_ SUBJECT \_ PREFIX** <br/> | <br/> |
   
6. サポートするメッセージ本文プロパティに区切り文字を追加します 。PR_BODY、PR_HTM L、または **PR_RTF_COMPRESSED。** 
    
7. [ScCreateConversationIndex](sccreateconversationindex.md)を呼び出し、元のメッセージのプロパティ[(PidTagConversationIndex)](pidtagconversationindex-canonical-property.md)プロパティPR_CONVERSATION_INDEX値を渡します。
    
8. 返信のプレフィックスを設定します。 標準の "RE:" を使用している場合は、これらの文字を **PR_NORMALIZED_SUBJECT** の先頭に連結し **、PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) をこの新しい文字列に設定します。 [(PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md) **PR_SUBJECT_PREFIX設定** しない。 3 文字を超える文字列など、標準以外のプレフィックスを使用している場合は、そのプレフィックスを **PR_SUBJECT_PREFIX。** 
    
9. プロパティの **PR_SENT_REPRESENTING** プロパティに対応する **値を設定** PR_RCVD_REPRESENTINGします。 
    
10. **PR \_ REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) および PR_REPLY RECIPIENT_NAMES ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) の各エントリを、プライマリ受信者のエントリ識別子と表示名 (型が MAPI_TO の受信者) に設定します。 **\_** これらのプロパティを同期します。 つまり **、PR_REPLY_RECIPIENT \_ ENTRYS** と **PR_REPLY_RECIPIENT_NAMES** には同じ数のエントリが含まれている必要があります。プロパティの 1 つの特定の位置にあるエントリは、他のプロパティの同じ位置にあるエントリに対応している必要があります。 
    
11. 返信が元のメッセージの送信者にのみ送信される場合は、元のメッセージの PR_SENT_REPRESENTING プロパティで表される受信者を含む 1 つの **エントリ受信者リストを作成** します。 受信者リストの作成の詳細については、「受信者リストの作成 [」を参照してください](creating-a-recipient-list.md)。
    
12. 返信が全員返信の場合は、次のように受信者リストを作成します。
    
    1. 元のメッセージの [IMessage::GetRecipientTable](imessage-getrecipienttable.md) メソッドを呼び出して、受信者テーブルにアクセスします。 
        
    2. [HrQueryAllRows を呼](hrqueryallrows.md)び出して、テーブル内のすべての行を取得します。 各行がプライマリ コピー受信者またはカーボン コピー受信者を表し、リストに残る必要がある場合、またはブラインド カーボン コピーの受信者またはユーザーを表し、リストから削除する必要があるかどうかを決定します。 
        
    3. 受信者の種類を区別するには、PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) 列を参照します。 この列は、プライマリ受信者MAPI_TO、カーボン コピー受信者MAPI_CC、ブラインド カーボン コピー受信者のMAPI_BCCに設定されます。 
        
    4. 元の **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 列を元のメッセージの **PR_RECEIVED_BY_SEARCH_KEY** プロパティと比較して、行がユーザーを表すかどうかを判断します。 
        
    5. [MAPIFreeBuffer](mapifreebuffer.md)を呼び出して受信者リストから不要な行を削除し、受信者テーブルの[SRowSet](srowset.md)構造内の対応するエントリに関連付けられているメモリを解放します。 プロパティ値配列のすべての値を 0 に設定し、すべての **cValues** メンバーを 0 に設定し **、SRowSet** の各 SRow 構造体のすべての **lpProps** メンバーを NULL に設定します。 [](srow.md) 
        
    6. 元のメッセージの **PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) および **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) プロパティで表される受信者リストに送信者を追加します。 一覧で送信者が重複していないか確認します。
        
    7. 返信メッセージの [IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを呼び出し  _、ulFlags_ パラメーターを 0 に設定して、元のメッセージのリストに基づいて返信メッセージまたは転送メッセージの新しい受信者リストを作成します。 
    
13. 返信の [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出してメッセージを保存するか [、IMessage::SubmitMessage](imessage-submitmessage.md) を呼び出して保存して送信します。 
    
> [!NOTE]
> **IMessage::ModifyRecipients** を呼び出して受信者リストに変更を保存する前に、ユーザーがメッセージ フォームを通じて変更を行うことができます。 ユーザーは、リストに追加するか、特定のメンバーを削除できます。 ユーザーが受信者リストに変更を加える許可は、オプションのクライアント機能です。 
  

