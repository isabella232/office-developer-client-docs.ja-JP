---
title: テーブルな内容
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0dd79d9630837b5ec8a709d386ccc0db987dfb5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799812"
---
# <a name="contents-tables"></a>テーブルな内容

  
  
**適用されます**: Outlook 
  
コンテンツ テーブルには、MAPI のコンテナー内のオブジェクトに関する情報が含まれています。 アドレス帳プロバイダーは、そのコンテナーのそれぞれのテーブルの内容を実装し、メッセージ ・ ストアとリモート トランスポート プロバイダーは、そのフォルダーの内容のテーブルを実装します。 アドレス帳コンテナーのコンテンツ テーブルは、フォルダーの内容のテーブル内のメッセージに関する情報を一覧表示中に、メッセージング ユーザーと配布リスト オブジェクトに関する情報を一覧表示します。 テーブルの内容は、主にクライアント アプリケーションによって使用されます。 
  
フォルダーの内容のテーブルの 2 種類があります。
  
- 標準的な内容のテーブルには、標準的なメッセージが含まれている、メッセージを送信し、ユーザーに表示できます。 
    
- コンテンツが関連付けられているテーブルには、によって作成されたクライアントの特定の目的のように標準的なメッセージの別の表現を格納する非表示の転送を可能な情報が含まれています。 関連情報は、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)の呼び出しに MAPI_ASSOCIATED フラグを渡すことによって作成されます。 
    
並べ替えテーブルのほとんどのアドレス帳コンテナーと多くのフォルダーをサポートしていない内容が分類されています。 
  
コンテンツ テーブルを呼び出すことによってアクセスできます。
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)。
    
    - または、
    
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) または**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (フォルダーのみ) プロパティ タグおよび IID として指定された[IMAPIProp::OpenProperty](imapiprop-openproperty.md)インターフェイス識別子として _IMAPITable。
    
メッセージ ストアとアドレス帳プロバイダーは、テーブルのプロパティを取得するため両方の方法をサポートする必要があります。 プロバイダーのいずれかを選択することがクライアントにこれらのテーブルをアクセスする方法の 1 つのみをサポートするために許容することはできません。 
  
 **GetContentsTable**は、環境設定を指定するいくつかのフラグを入力として受け取ります。 設定すると、MAPI_ASSOCIATED フラグは、関連付けられている内容のテーブルを取得します。 このオプションをいくつかのフォルダーでは、関連付けられている内容をサポートしていないクライアントがこれを事前に決定するための手段がないため、要求されると、関連付けられているコンテンツのテーブルにも、 **GetContentsTable**は MAPI_E_NO_SUPPORT のエラーを返します。 
  
MAPI_DEFERRED_ERRORS フラグは、呼び出し時に検出されたエラーは、後で報告する必要はありませんが、テーブルを実装することを示します。 
  
**IMAPIProp::OpenProperty**への呼び出しでは、アドレス帳の内容のテーブルおよび標準的なフォルダーの内容のテーブル、および**PR_FOLDER_ASSOCIATED_ の**PR_CONTAINER_CONTENTS**を、対応するプロパティを開いて、内容のテーブルへのアクセス内容**の内容のテーブルを関連付けられています。 どちらがフォルダーまたはコンテナーの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドによってこれらのプロパティを取得することができます、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返されるプロパティ タグ配列に含まれているか。 
  
 **PR_CONTAINER_CONTENTS**は、コピー操作の内容のテーブルをエクスクルードまたはインクルードするにも使用できます。 クライアントは、コピー操作で**IMAPIProp::CopyTo**の*lpExcludeProps*パラメーターでの**PR_CONTAINER_CONTENTS**を指定した場合、新しいフォルダーまたはコンテナーはサポートされません、元のフォルダーまたはコンテナーのコンテンツ テーブル。 
  
アドレス帳コンテナー、フォルダーの内容のテーブルに必要な列の長いリストがあります: 列**GetContentsTable**または**OpenProperty**からテーブルを検索した後に、使用するクライアントが求めることができます。 プロバイダーは、必要に応じて、 **SetColumns**メソッドをクライアントでは、要求することも変更する場合、必要なこのセットに追加できます。 
  
コンテンツ テーブルの種類ごとに必要な列は次のとおりです。
  
|**必要な列**|**コンテンツ テーブルの種類**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |アドレス帳コンテナー  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |アドレス帳コンテナー  <br/> |
|**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
|**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |アドレス帳コンテナー  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |すべてのテーブルな内容  <br/> |
|**PR_HASATTACH**([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |すべてのテーブルな内容  <br/> |
|**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
|**PR_MAPPING_SIGNATURE**([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
|**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |フォルダーのテーブルにリモート トランスポート  <br/> |
|**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_MSG_STATUS**([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |すべてのテーブルな内容  <br/> |
|**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |アドレス帳コンテナーと、メッセージ フォルダー テーブルを格納します。  <br/> |
|**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |フォルダーのテーブルにリモート トランスポート  <br/> |
|**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
|**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
   
それぞれの行で使用可能なエントリの識別子は、短期または長期のエントリ id、テーブルの実装によってどちらでもかまいません。 短期的なエントリ id は通常、パフォーマンスに問題がある場合に使用します。 エントリ id のいずれかのタイプは、対応するオブジェクトへのアクセスに使用できます。 
  
内容のテーブルでは、省略可能ですが、サービス ・ プロバイダーの実装で、一般的に含まれている列のセットもあります。 これらの省略可能な列は次のとおりです。
  
|**省略可能な列**|**コンテンツ テーブルの種類**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
|**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |標準的なフォルダーの内容のテーブル  <br/> |
|**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |標準的なフォルダーの内容のテーブル  <br/> |
|**PR_CONVERSATION_INDEX**([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |メッセージ ストアのフォルダー テーブル  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |アドレス帳コンテナー  <br/> |
|**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |アドレス帳コンテナー  <br/> |
|**PR_SEND_RICH_INFO**([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |アドレス帳コンテナー  <br/> |
|**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |すべてのフォルダーの内容のテーブル  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |アドレス帳コンテナー  <br/> |
   
メッセージ ストア プロバイダーは、検索結果フォルダーの内容のテーブルのみの**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) をも含める必要があります。
  
フォルダー内のすべてのメッセージ同じシグネチャを持つマッピング、つまり、同じ識別子のプロパティをプロパティ名のマッピングの場合にのみ、フォルダーの内容のテーブルの列に名前付きプロパティを追加する場合があります。 フォルダー内の任意のメッセージの作成をサポートする場合、フォルダーの内容のテーブルには列に固有のプロパティを設定する追加のメッセージ クラスをサポートしなければなりません。
  
クライアントは、その[IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)メソッドを呼び出して、フォルダーの内容のテーブルの既定の並べ替え順序を保存できます。 呼び出しで、RECURSIVE_SORT フラグを指定する場合は、フォルダー内のサブフォルダーのすべてに適用する並べ替え順序を作成できます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

