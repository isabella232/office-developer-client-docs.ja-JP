---
title: IMessage imapiprop
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 217411dc8bae12a3d7544a4cfd189c4c8f863195
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432500"
---
# <a name="imessage--imapiprop"></a>IMessage : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ、添付ファイル、および受信者を管理します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |Message オブジェクト  <br/> |
|実装元:  <br/> |メッセージストアプロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMessage  <br/> |
|ポインターの種類:  <br/> |lpmessage  <br/> |
|トランザクションモデル:  <br/> |一括  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[getattachmenttable](imessage-getattachmenttable.md) <br/> |メッセージの添付ファイルテーブルを返します。  <br/> |
|[openattach](imessage-openattach.md) <br/> |添付ファイルを開きます。  <br/> |
|[createattach](imessage-createattach.md) <br/> |新しい添付ファイルを作成します。  <br/> |
|[deleteattach](imessage-deleteattach.md) <br/> |添付ファイルを削除します。  <br/> |
|[get受信者テーブル](imessage-getrecipienttable.md) <br/> |メッセージの recipient テーブルを返します。  <br/> |
|[modifyrecipients](imessage-modifyrecipients.md) <br/> |�ǉ��A�폜�A�܂��̓��b�Z�[�W�̎�M�҂�ύX���܂��B  <br/> |
|[submitmessage](imessage-submitmessage.md) <br/> |メッセージに加えられたすべての変更を保存し、送信の準備ができたことをマークします。  <br/> |
|[setreadflag](imessage-setreadflag.md) <br/> |メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、閲覧レポートの送信を管理します。  <br/> |
   
次のプロパティは、ライフサイクルのある時点でのメッセージに必要です。 読み取り専用プロパティのほとんどは、クライアントがメッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出したときに、メッセージストアプロバイダーによって設定されます。 その他の読み取り専用プロパティは、トランスポートプロバイダーによって設定されます。 
  
|**すべてのクラスのメッセージに必要なプロパティ**|**Access**|
|:-----|:-----|
|**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
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
   
次のプロパティはすべて、クライアントに対して読み取り専用になっており、 **PR_BODY**は例外です。 クライアントは、レポートを処理するときにこのプロパティを作成します。
  
|**レポートメッセージのプロパティ**|
|:-----|
|**PR_BODY**([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |
|**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))  <br/> |
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
|**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
|**メッセージ受信者のプロパティ**|**Access**|**必須または省略可能**|
|:-----|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |読み取り専用  <br/> |必須  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |必須  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |必須  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |読み取り専用  <br/> |省略可能  <br/> |
|**PR_ENTRYID** <br/> |読み取り専用  <br/> |必須  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |必須  <br/> |
|**PR_SEARCH_KEY** <br/> |読み取り専用  <br/> |省略可  <br/> |
   

