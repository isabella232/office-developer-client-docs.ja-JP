---
title: 目次テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435587"
---
# <a name="contents-tables"></a>目次テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
contents テーブルには、MAPI コンテナー内のオブジェクトに関する情報が含まれています。 アドレス帳プロバイダーは、コンテナーごとにコンテンツテーブルを実装し、メッセージストアプロバイダーとリモートトランスポートプロバイダーはフォルダーにコンテンツテーブルを実装します。 アドレス帳コンテナーの contents テーブルには、そのメッセージングユーザーおよび配布リストオブジェクトに関する情報が一覧表示されますが、フォルダーのコンテンツテーブルには、そのメッセージに関する情報が表示されます。 コンテンツテーブルは、主にクライアントアプリケーションによって使用されます。 
  
フォルダーコンテンツテーブルには、次の2種類があります。
  
- 標準のコンテンツテーブルには、標準メッセージ (送信可能でユーザーに対して表示可能なメッセージ) が含まれています。 
    
- [関連付けられたコンテンツ] テーブルには、標準メッセージの代替表現を格納するなど、特定の目的のためにクライアントによって作成された隠し、非対応のテーブル情報が含まれています。 関連情報は、MAPI_ASSOCIATED フラグを[imapifolder:: CreateMessage](imapifolder-createmessage.md)呼び出しに渡すことによって作成されます。 
    
ほとんどのアドレス帳コンテナーの内容テーブルと多くのフォルダーは、分類された並べ替えをサポートしていません。 
  
コンテンツテーブルには、次の呼び出しを使用してアクセスできます。
  
- [IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)。
    
    - や
    
- [imapiprop:: openproperty](imapiprop-openproperty.md) with **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) または**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (folders のみ) をプロパティタグと IID として指定します。_ IMAPITable をインターフェイス識別子として入力します。
    
メッセージストアプロバイダーとアドレス帳プロバイダーは、テーブルプロパティを取得するための両方の手法をサポートする必要があります。 クライアントが選択を必要とするため、プロバイダーはこれらのテーブルにアクセスする方法を1つだけサポートすることはできません。 
  
 **getcontentstable**は、設定を指定するいくつかのフラグを入力として受け取ります。 設定すると、MAPI_ASSOCIATED フラグは、関連付けられたコンテンツテーブルを取得します。 一部のフォルダーは関連付けられたコンテンツをサポートしておらず、クライアントがこれを事前に決定する方法がないため、 **getcontentstable**は、関連付けられた contents テーブルが要求されたときに、error MAPI_E_NO_SUPPORT を返すことがあります。 
  
MAPI_DEFERRED_ERRORS フラグは、呼び出し中に発生したエラーを後で報告する必要がないことを表の実装側に示します。 
  
**imapiprop:: openproperty**の呼び出しでは、対応するプロパティ、 **PR_CONTAINER_CONTENTS** address book contents tables および標準フォルダーコンテンツテーブル、および PR_FOLDER_ASSOCIATED_ を開くことによって、contents テーブルにアクセスする必要があります。 **** 関連付けられたコンテンツテーブルのコンテンツ。 これらのプロパティは、フォルダーまたはコンテナーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して取得することはできませんが、これらは[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返される property タグ配列に含まれています。 
  
 **PR_CONTAINER_CONTENTS**を使用して、コピー操作の内容テーブルを追加または除外することもできます。 クライアントが**imapiprop:: CopyTo**の*lpexcludeprops*パラメーターで**PR_CONTAINER_CONTENTS**を指定している場合、コピー操作では、新しいフォルダーまたはコンテナーは、元のフォルダーまたはコンテナーの CONTENTS テーブルをサポートしません。 
  
アドレス帳のコンテナーとフォルダーの内容のテーブルには、必要な列の長いリストがあります。これは、 **getcontentstable**または**openproperty**からテーブルを取得した後で、クライアントが使用できるようにする列です。 プロバイダーは必要に応じてこの必須セットを追加でき、 **SetColumns**メソッドを介してクライアントが変更を要求することもできます。 
  
各種類の目次テーブルに必要な列は次のとおりです。
  
|**必要な列**|**目次表の種類**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |アドレス帳のコンテナーテーブル  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |アドレス帳のコンテナーテーブル  <br/> |
|**PR_DISPLAY_CC**([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
|**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |アドレス帳のコンテナーテーブル  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |すべてのコンテンツの表  <br/> |
|**PR_HASATTACH**([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |すべてのコンテンツの表  <br/> |
|**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
|**PR_MAPPING_SIGNATURE**([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
|**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |リモートトランスポートフォルダーの表  <br/> |
|**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_MSG_STATUS**([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |すべてのコンテンツの表  <br/> |
|**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |アドレス帳のコンテナーとメッセージストアのフォルダーテーブル  <br/> |
|**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |リモートトランスポートフォルダーの表  <br/> |
|**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
|**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
   
各行で使用できるエントリ識別子は、テーブルの実装に応じて、短い、または長い用語のエントリ識別子にすることができます。 短期エントリ識別子は、通常、パフォーマンスが問題になる状況で使用されます。 どちらの種類のエントリ識別子を使用しても、対応するオブジェクトにアクセスできます。 
  
コンテンツテーブルには、オプションではなく、サービスプロバイダーによって一般的に実装される列のセットもあります。 オプションの列は次のとおりです。
  
|**省略可能な列**|**目次表の種類**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
|**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |標準フォルダーコンテンツテーブル  <br/> |
|**PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |標準フォルダーコンテンツテーブル  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |メッセージストアのフォルダーテーブル  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |アドレス帳のコンテナーテーブル  <br/> |
|**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |アドレス帳のコンテナーテーブル  <br/> |
|**PR_SEND_RICH_INFO**([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |アドレス帳のコンテナーテーブル  <br/> |
|**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |すべてのフォルダーコンテンツテーブル  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |アドレス帳のコンテナーテーブル  <br/> |
   
また、メッセージストアプロバイダーには、 **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) の検索結果フォルダーのコンテンツテーブルのみが含まれている必要があります。
  
名前付きプロパティは、フォルダー内のすべてのメッセージが同じマッピング署名 (プロパティ名とプロパティ識別子のマッピング) を持つ場合にのみ、フォルダーのコンテンツテーブルの列セットに追加されることがあります。 フォルダーコンテンツテーブルでは、フォルダー内での任意のメッセージの作成をサポートしている場合に、メッセージクラス固有のプロパティを列セットに追加することがサポートされている必要があります。
  
クライアントは、 [imapifolder:: SaveContentsSort](imapifolder-savecontentssort.md)メソッドを呼び出すことによって、フォルダーコンテンツテーブルの既定の並べ替え順序を保存できます。 呼び出しで RECURSIVE_SORT フラグが指定されている場合は、そのフォルダー内のすべてのサブフォルダーに適用する並べ替え順序を設定できます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

