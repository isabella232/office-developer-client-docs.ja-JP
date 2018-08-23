---
title: IMessage IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage
api_type:
- COM
ms.assetid: 7e244d40-595e-432c-aa8c-f9f62ca3c138
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b594297d364ba4f5a3ff7da603d2fe7c2fe8cf07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588532"
---
# <a name="imessage--imapiprop"></a>IMessage : IMAPIProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ、添付ファイル、および受信者を管理します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |Message オブジェクト  <br/> |
|によって実装されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMessage  <br/> |
|ポインターの型。  <br/> |LPMESSAGE  <br/> |
|トランザクション モデル:  <br/> |トランザクション処理  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetAttachmentTable](imessage-getattachmenttable.md) <br/> |メッセージの添付ファイル テーブルを返します。  <br/> |
|[OpenAttach](imessage-openattach.md) <br/> |添付ファイルを開きます。  <br/> |
|[CreateAttach](imessage-createattach.md) <br/> |新しい添付ファイルを作成します。  <br/> |
|[DeleteAttach](imessage-deleteattach.md) <br/> |添付ファイルを削除します。  <br/> |
|[GetRecipientTable](imessage-getrecipienttable.md) <br/> |メッセージの受信者テーブルを取得します。  <br/> |
|[ModifyRecipients](imessage-modifyrecipients.md) <br/> |�ǉ��A�폜�A�܂��̓��b�Z�[�W�̎�M�҂�ύX���܂��B  <br/> |
|[SubmitMessage](imessage-submitmessage.md) <br/> |メッセージのすべての変更内容を保存し、送信の準備が完了としてマークを付けます。  <br/> |
|[SetReadFlag](imessage-setreadflag.md) <br/> |設定し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティに MSGFLAG_READ フラグをクリアまたはリードのレポートの送信を管理します。  <br/> |
   
そのライフ サイクル中にいくつかの時点でメッセージの次のプロパティが必要です。 読み取り専用プロパティのほとんどは、クライアントがメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すと、メッセージ ストア プロバイダーによって設定されます。 その他の読み取り専用プロパティは、トランスポート プロバイダーによって設定されています。 
  
|**クラスのすべてのメッセージに必要なプロパティ**|**Access**|
|:-----|:-----|
|**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_CC_ME**([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_RECIP_ME**([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_TO_ME**([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_ORIGINATOR**プロパティ  <br/> |読み取り専用  <br/> |
|**PR_PARENT_DISPLAY**([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECEIVED_BY**プロパティ  <br/> |読み取り専用  <br/> |
|**PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_SENDER**プロパティ  <br/> |読み取り専用  <br/> |
|**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
次のプロパティはすべて読み取り専用**PR_BODY**以外のクライアントには。 クライアントは、レポートを処理する際に、このプロパティを作成します。
  
|**レポート メッセージのプロパティ**|
|:-----|
|**PR_BODY**([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**PR_CONVERSATION_INDEX**([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |
|**PR_CONVERSATION_TOPIC**([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))  <br/> |
|**PR_MESSAGE_CLASS** <br/> |
|**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME**([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_BCC**([PidTagOriginalDisplayBcc](pidtagoriginaldisplaybcc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_CC**([PidTagOriginalDisplayCc](pidtagoriginaldisplaycc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_TO**([PidTagOriginalDisplayTo](pidtagoriginaldisplayto-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBJECT**([PidTagOriginalSubject](pidtagoriginalsubject-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBMIT_TIME**([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md))  <br/> |
|**PR_REPORT_TAG**([PidTagReportTag](pidtagreporttag-canonical-property.md))  <br/> |
|**PR_REPORT_TEXT**([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |
|**PR_REPORT_TIME**([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |
|**PR_SEARCH_KEY** <br/> |
|**PR_SENDER**プロパティ  <br/> |
|**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
|**メッセージの受信者のプロパティ**|**Access**|**必須または省略可能です**|
|:-----|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |読み取り専用  <br/> |必須  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |必須  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |必須  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |読み取り専用  <br/> |省略可能  <br/> |
|**PR_ENTRYID** <br/> |読み取り専用  <br/> |必須  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |必須  <br/> |
|**PR_SEARCH_KEY** <br/> |読み取り専用  <br/> |省略可能  <br/> |
   

