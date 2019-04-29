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
  
クライアントアプリケーションは、通常、元のメッセージの送信者にのみ送信される返信と、元のメッセージの受信者リストに含まれている他のすべての受信者に送信される2種類の返信をサポートします。 この2番目の返信の種類は、通常、全員に返信メッセージと呼ばれます。
  
いずれかの種類の返信を送信するには、元のメッセージを送信する場合と同じようなタスクをいくつか実装します。 たとえば、既定のメッセージストアと送信メッセージフォルダー (通常は送信トレイ) を開き、送信フォルダーの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出して返信を作成します。 また、元のメッセージを保持するフォルダー (通常は受信トレイ) を開きます。 別のフォルダーを開く方法については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。
  
返信を作成し、元のメッセージを作成する場合の主な違いは、返信の場合、プロパティのほとんどは元のメッセージのプロパティから直接またはコピーすることです。 添付ファイル-メッセージの**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティは、特に除外されています。 すべての返信メッセージの受信者リストは、元のメッセージの一覧から、 **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) プロパティによって表される受信者と、すべてのブラインドカーボンコピー受信者が削除されて作成されます。 **PR_RECEIVED_BY_SEARCH_KEY**プロパティは、現在のユーザーを表します。 
  
### <a name="to-send-a-reply"></a>返信を送信するには
  
1. 既定のメッセージストアを開きます。 詳細については、「[既定のメッセージストアを開く](opening-the-default-message-store.md)」を参照してください。
    
2. [送信トレイ] フォルダーを開きます。 詳細については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。
    
3. 送信トレイの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出して、返信を作成します。 
    
4. 元のメッセージの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、次のプロパティを返信メッセージにコピーします。 
    
   - **リッチ\_** テキスト形式をサポートしているかどうかに応じて、PR 本文 ([PidTagBody](pidtagbody-canonical-property.md)) または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))。
    
   - **[\_PR MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) (応答が受信者一覧全体に送られる場合)。
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
5. **imapiprop:: CopyTo**に対する呼び出しには、次のプロパティを含めないでください。
    
    |||
    |:-----|:-----|
    |**PR\_クライアント\_送信\_時刻** <br/> |**PR\_メッセージ\_の\_配信時間** <br/> |
    |**PR\_メッセージ\_の\_ダウンロード時間** <br/> |**PR\_メッセージ\_フラグ** <br/> |
    |**PR\_発信\_者\_配信レポート \ 要求** <br/> |**プロパティ\_を\_表す PR RCVD**  <br/> |
    |**PR\_開封\_確認\_の ENTRYID** <br/> |**PR\_開封\_確認\_メッセージの要求** <br/> |
    |**PR\_BY\_プロパティで受信**  <br/> |**PR\_応答\_受信者**プロパティ  <br/> |
    |**PR\_レポート\_の ENTRYID** <br/> |**PR\_SENDER**のプロパティ  <br/> |
    |**PR\_送信\_され**たプロパティ  <br/> |**PR\_送信メール\_の ENTRYID** <br/> |
    |**PR\_件名\_の接頭辞** <br/> | <br/> |
   
6. サポートするメッセージ本文のプロパティ ( **PR_BODY**、 **PR_HTM**L、 **PR_RTF_COMPRESSED**) に区切り文字を追加します。
    
7. [ScCreateConversationIndex](sccreateconversationindex.md)を呼び出し、元のメッセージの**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティの値を渡します。
    
8. 返信のプレフィックスを設定します。 標準の "RE:" を使用している場合は、これらの文字を**PR_NORMALIZED_SUBJECT**の先頭に連結し、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) をこの新しい文字列に設定します。 **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) を設定しません。 3文字を超える文字列など、標準的ではないプリフィックスを使用している場合は、 **PR_SUBJECT_PREFIX**に格納します。 
    
9. **PR_SENT_REPRESENTING**プロパティを**PR_RCVD_REPRESENTING**プロパティの対応する値に設定します。 
    
10. **PR\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) および**\_PR_REPLY RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) の各エントリを、エントリ id およびの表示名に設定します。プライマリ受信者— MAPI_TO の種類の受信者。 これらのプロパティを同期したままにします。 つまり、 **PR_REPLY_RECIPIENT\_** entry と**PR_REPLY_RECIPIENT_NAMES**には同じ数のエントリが含まれている必要があり、いずれかのプロパティ内の特定の位置にあるエントリは、もう一方の同じ位置にあるエントリに対応している必要があります。プロパティ. 
    
11. 返信が元のメッセージの送信者にのみ送信されている場合は、元のメッセージの**PR_SENT_REPRESENTING**プロパティによって表される受信者リストを1つ作成します。 受信者リストの作成の詳細については、「[受信者リストを作成](creating-a-recipient-list.md)する」を参照してください。
    
12. 返信が全員に返信の場合は、次のように受信者リストを作成します。
    
    1. 元のメッセージの[IMessage:: get受信者 table](imessage-getrecipienttable.md)メソッドを呼び出して、その受信者テーブルにアクセスします。 
        
    2. [hrqueryallrows](hrqueryallrows.md)を呼び出して、テーブル内のすべての行を取得します。 各行がプライマリまたはカーボンコピーの受信者を表しているかどうかを判断し、リストに残すか、または bcc 受信者またはユーザーを表す場合は、リストから削除する必要があります。 
        
    3. 受信者の種類を区別するには、 **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) 列を参照してください。 この列は、プライマリ受信者の場合は MAPI_TO、カーボンコピー受信者の場合は MAPI_CC、ブラインドカーボンコピーの受信者の場合は MAPI_BCC に設定されます。 
        
    4. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 列を元のメッセージの**PR_RECEIVED_BY_SEARCH_KEY**プロパティと比較して、その行がユーザーを表しているかどうかを判断します。 
        
    5. 受信者リストから不要な行を削除するには、 [MAPIFreeBuffer](mapifreebuffer.md)を呼び出して、受信者テーブルの[srowset](srowset.md)構造内の対応するエントリに関連付けられているメモリを解放します。 プロパティ値の配列のすべての値を0に、すべての**cvalues**メンバーを0に、 **srow**内の各[srow](srow.md)構造のすべての**lpprops**メンバーを NULL に設定します。 
        
    6. 元のメッセージの**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) および**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) によって表される受信者リストに送信者を追加します。プロパティ. 送信者が一覧に複製されていないことを確認します。
        
    7. 返信メッセージの[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出し、 _ulflags_パラメーターを0に設定して、元のメッセージのリストに基づいて、返信または転送されたメッセージの新しい受信者リストを作成します。 
    
13. 返信の[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、メッセージまたは[IMessage:: submitmessage](imessage-submitmessage.md)を保存し、送信します。 
    
> [!NOTE]
> **IMessage:: modifyrecipients**を呼び出して、受信者一覧に変更内容を格納する前に、ユーザーがメッセージフォームで変更できるようにすることができます。 ユーザーは、リストに追加したり、特定のメンバーを削除したりできます。 ユーザーが受信者リストを変更できるようにすることは、オプションのクライアント機能です。 
  

