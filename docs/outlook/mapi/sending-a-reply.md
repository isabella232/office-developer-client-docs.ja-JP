---
title: 返信を送信
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d83fce761afb4673b71df9d620ac3fd794d6009f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803843"
---
# <a name="sending-a-reply"></a>返信を送信

**適用対象**: Outlook 
  
クライアント アプリケーションは、通常、返信の 2 つの種類をサポートします。 元のメッセージと送信者だけでなく、元のメッセージの受信者のリストに含まれている他のすべての受信者に送信される 1 つの送信者にのみ送信される 1 つ。 この 2 つ目の種の応答は、すべてのメッセージの返信とも呼ばれます。
  
いずれかのタイプの応答を送信するには、元のメッセージを送信するときと同様のタスクの一部を実装します。 などの既定のメッセージ ストアを開き、送信メッセージのフォルダー、通常、[送信トレイ]、および、返信を作成するのには、送信フォルダーの[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 また、受信トレイでは通常、元のメッセージを保持しているフォルダーを開きます。 別のフォルダーを開く方法については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。
  
返信を作成し、元のメッセージを作成するには大きな違いは、ことで、返信のプロパティのほとんどはに基づいてまたは元のメッセージのプロパティから直接コピーします。 添付ファイル、メッセージの**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティ-明示的に除外されています。 **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) のプロパティで表される受信者およびすべてのブラインド カーボン コピー受信者を削除すると元のメッセージの一覧からすべてのメッセージが作成した返信の受信者の一覧です。 **PR_RECEIVED_BY_SEARCH_KEY**プロパティは、現在のユーザーを表します。 
  
### <a name="to-send-a-reply"></a>返信を送信するには
  
1. 既定のメッセージ ストアを開きます。 詳細については、[既定のメッセージ ストアを開く](opening-the-default-message-store.md)を参照してください。
    
2. [送信トレイ] フォルダーを開きます。 詳細については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。
    
3. 返信を作成するのには、[送信トレイ] の[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 
    
4. 返信メッセージに次のプロパティをコピーするのには、元のメッセージの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。 
    
   - **PR\_本体**([PidTagBody](pidtagbody-canonical-property.md)) または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) は、リッチ テキスト形式をサポートするかどうかによって異なります。
    
   - **PR\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))、全体のアドレス帳への返信になる場合。
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))。
    
5. **IMAPIProp::CopyTo**を呼び出すには次のプロパティは含まれません。
    
    |||
    |:-----|:-----|
    |**PR\_クライアント\_送信\_時間** <br/> |**PR\_メッセージ\_配信\_時間** <br/> |
    |**PR\_メッセージ\_をダウンロード\_時間** <br/> |**PR\_メッセージ\_フラグ** <br/> |
    |**PR\_作成者\_配信\_REPORT\REQUESTED** <br/> |**PR\_受信数\_REPRESENTING**のプロパティ  <br/> |
    |**PR\_読み取り\_入荷\_エントリ ID** <br/> |**PR\_読み取り\_入荷\_要求されました。** <br/> |
    |**PR\_受信\_で**のプロパティ  <br/> |**PR\_返信\_受信者**のプロパティ  <br/> |
    |**PR\_レポート\_エントリ ID** <br/> |**PR\_送信者**のプロパティ  <br/> |
    |**PR\_送信\_REPRESENTING**のプロパティ  <br/> |**PR\_SENTMAIL\_エントリ ID** <br/> |
    |**PR\_件名\_プレフィックス** <br/> | <br/> |
   
6. どちらをサポートするメッセージ本文のプロパティに区切り記号のテキストを追加: **PR_BODY**、 **PR_HTM**L、または**PR_RTF_COMPRESSED**。
    
7. [ScCreateConversationIndex](sccreateconversationindex.md)、元のメッセージの**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) のプロパティの値を渡してを呼び出します。
    
8. 返信のプレフィックスを設定します。 標準を使用している場合"RE:"、 **PR_NORMALIZED_SUBJECT**の先頭にこれらの文字を連結し、この新しい文字列に**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) を設定します。 **されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) を設定することはしません。 3 文字より長い文字列などの非標準のプレフィックスを使用している場合は、**されて**に格納します。 
    
9. **PR_RCVD_REPRESENTING**プロパティに対応する値には、 **PR_SENT_REPRESENTING**プロパティを設定します。 
    
10. 設定のエントリの各**PR\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) と**PR_REPLY\_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) のエントリの識別子および表示名に、プライマリ受信者、受信者の種類は、MAPI_TO です。 これらのプロパティが同期を維持します。 **PR_REPLY_RECIPIENT\_エントリ**と**PR_REPLY_RECIPIENT_NAMES**には、同じ数のエントリが含まれている必要があり、プロパティのいずれかの特定の位置にあるエントリが、他の同じ位置にあるエントリを対応する必要がありますプロパティです。 
    
11. 返信は、元のメッセージの送信者にのみ送信されるが場合、は、元のメッセージの**PR_SENT_REPRESENTING**プロパティで表され、受信者と 1 つのエントリのアドレス帳を作成します。 受信者リストの作成の詳細については、[受信者リストを作成する](creating-a-recipient-list.md)を参照してください。
    
12. 応答がすべての返信の場合は、次のように受信者の一覧を作成します。
    
    1. 受信者テーブルにアクセスするための元のメッセージの[IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出します。 
        
    2. すべてのテーブルの行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。 ブラインド カーボン コピー受信者またはユーザーを表し、リストから削除する必要がある場合は、各行の主キー列またはカーボン コピー受信者を表すし、のリストを保持する必要がありますかを決定します。 
        
    3. **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) の列を参照して受信者の種類を区別します。 この列は、そのカーボン コピー受信者、および MAPI_BCC のブラインド カーボン コピー受信者のプライマリ受信者用の MAPI_TO、MAPI_CC に設定されます。 
        
    4. 行がユーザーを表すかどうかを確認する元のメッセージの**PR_RECEIVED_BY_SEARCH_KEY**プロパティを使用して**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) の列を比較します。 
        
    5. 受信者テーブルの[SRowSet](srowset.md)構造内の対応するエントリに関連付けられているメモリを解放する[MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことによって、受信者の一覧から不要な行を削除します。 **SRowSet**内の個々 の[SRow](srow.md)構造体の**lpProps**メンバーの値がゼロにすべての値がゼロに**あう**メンバー プロパティの値の配列内の値のすべてとは NULL に設定します。 
        
    6. によって元のメッセージの受信者の一覧に送信者を追加**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) と**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))プロパティです。 送信者が、ボックスの一覧で重複していないことを確認してください。
        
    7. _UlFlags_パラメーターを返信用の新しい受信者一覧を作成するのには、0 に設定、元のメッセージの一覧を基にメッセージを転送または返信メッセージの[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出します。 
    
13. [IMessage::SubmitMessage](imessage-submitmessage.md)を保存し、送信するメッセージを保存するのには、返信の[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
> [!NOTE]
> アドレス帳の変更を格納する**IMessage::ModifyRecipients**を呼び出す前に、メッセージ フォームを変更するユーザーを許可できます。 ユーザーでは、リストに追加したり、特定のメンバーを削除することができます。 受信者のリストを変更するユーザーを許可する、省略可能なクライアント機能です。 
  

