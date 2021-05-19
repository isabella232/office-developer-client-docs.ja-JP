---
title: コンテンツ テーブル
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
# <a name="contents-tables"></a>コンテンツ テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテンツ テーブルには、MAPI コンテナー内のオブジェクトに関する情報が含まれています。 アドレス帳プロバイダーは各コンテナーのコンテンツ テーブルを実装し、メッセージ ストアとリモート トランスポート プロバイダーはフォルダーのコンテンツ テーブルを実装します。 アドレス帳コンテナーのコンテンツ テーブルには、メッセージング ユーザーおよび配布リスト オブジェクトに関する情報が一覧表示され、フォルダーのコンテンツ テーブルにはメッセージに関する情報が一覧表示されます。 コンテンツ テーブルは、主にクライアント アプリケーションで使用されます。 
  
フォルダーコンテンツ テーブルには、次の 2 種類があります。
  
- 標準コンテンツ テーブルには、標準メッセージ (ユーザーに送信および表示できるメッセージ) が含まれます。 
    
- 関連付けられたコンテンツ テーブルには、標準メッセージの代替表現を格納するなど、特定の目的のためにクライアントによって作成された非表示の送信不可の情報が含まれます。 関連付けられた情報は [、IMAPIFolder::CreateMessage](imapifolder-createmessage.md) 呼び出しに MAPI_ASSOCIATEDフラグを渡して作成されます。 
    
ほとんどのアドレス帳コンテナーと多くのフォルダーのコンテンツ テーブルでは、分類された並べ替えはサポートされていません。 
  
コンテンツ テーブルには、次の呼び出しでアクセスできます。
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Or -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) と **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) または **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (フォルダーのみ) をプロパティ タグとして指定し、IID_IMAPITable をインターフェイス識別子として指定します。
    
メッセージ ストアプロバイダーとアドレス帳プロバイダーは、テーブル プロパティを取得するための両方の手法をサポートする必要があります。 クライアントが選択肢を持つ必要がある場合に、プロバイダーがこれらのテーブルにアクセスするための 1 つの方法のみをサポートすることはできません。 
  
 **GetContentsTable は** 、基本設定を指定する複数のフラグを入力として受け入れる。 このフラグを設定すると、MAPI_ASSOCIATED関連付けられたコンテンツ テーブルが取得されます。 一部のフォルダーは関連付けられたコンテンツをサポートしていないため、クライアントがこれを事前に判断する方法がないので、関連付けられたコンテンツ テーブルが要求された場合 **、GetContentsTable** はエラー MAPI_E_NO_SUPPORT を返す場合があります。 
  
[MAPI_DEFERRED_ERRORS] フラグは、呼び出し中に発生したエラーを後で報告する必要がなことを表の実装者に示します。 
  
**IMAPIProp::OpenProperty** の呼び出しでは、対応するプロパティを開いてコンテンツ テーブルにアクセスし、アドレス帳のコンテンツ テーブルと標準フォルダー コンテンツ テーブルの **PR_CONTAINER_CONTENTS、** 関連するコンテンツ テーブルの **PR_FOLDER_ASSOCIATED_CONTENTS** にアクセスします。 フォルダーまたはコンテナーの[IMAPIProp::GetProps メソッドを使用して取得することはできませんが、IMAPIProp::GetPropList](imapiprop-getprops.md)メソッドによって返されるプロパティ タグ配列に含[](imapiprop-getproplist.md)まれます。 
  
 **PR_CONTAINER_CONTENTS** を使用して、コピー操作からコンテンツ テーブルを含めるか除外することができます。 クライアントがコピー **操作で** **IMAPIProp::CopyTo** の *lpExcludeProps* パラメーターに PR_CONTAINER_CONTENTS を指定した場合、新しいフォルダーまたはコンテナーは元のフォルダーまたはコンテナーのコンテンツ テーブルをサポートしない。 
  
アドレス帳コンテナーおよびフォルダーコンテンツ テーブルには **、GetContentsTable** または **OpenProperty** からテーブルを取得した後にクライアントが使用できる列など、必要な列の長い一覧があります。 プロバイダーは必要に応じてこの必須セットに追加できます。また、 **クライアントは SetColumns** メソッドを使用して変更を要求できます。 
  
コンテンツ テーブルの種類ごとに必要な列は次のとおりです。
  
|**必須列**|**コンテンツ テーブルの種類**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |アドレス帳コンテナー テーブル  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |アドレス帳コンテナー テーブル  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |アドレス帳コンテナー テーブル  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |すべてのコンテンツ テーブル  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |すべてのコンテンツ テーブル  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |リモート トランスポート フォルダー テーブル  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |すべてのコンテンツ テーブル  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |アドレス帳コンテナーとメッセージ ストア フォルダー テーブル  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |リモート トランスポート フォルダー テーブル  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
   
各行で使用できるエントリ識別子は、テーブルの実装に応じて、短いエントリ識別子または長期エントリ識別子のいずれかになります。 通常、短期的なエントリ識別子は、パフォーマンスが問題である状況で使用されます。 いずれかの種類のエントリ識別子を使用して、対応するオブジェクトにアクセスできます。 
  
コンテンツ テーブルには、オプションですが、一般的にサービス プロバイダーが実装に含める一連の列があります。 これらの省略可能な列は次のとおりです。
  
|**省略可能な列**|**コンテンツ テーブルの種類**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |標準のフォルダーコンテンツ テーブル  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |標準のフォルダーコンテンツ テーブル  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |メッセージ ストア のフォルダー テーブル  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |アドレス帳コンテナー テーブル  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |アドレス帳コンテナー テーブル  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |アドレス帳コンテナー テーブル  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |すべてのフォルダーコンテンツ テーブル  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |アドレス帳コンテナー テーブル  <br/> |
   
また、検索結果フォルダーのコンテンツ テーブル **PR_PARENT_DISPLAYには、** メッセージ ストア プロバイダーに 、PR_PARENT_DISPLAY ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) を含める必要があります。
  
フォルダー内のすべてのメッセージが同じマッピング署名 、つまりプロパティ名とプロパティ識別子の同じマッピングを持っている場合にのみ、名前付きプロパティをフォルダーコンテンツ テーブルの列セットに追加できます。 フォルダー内の任意のメッセージの作成をサポートしている場合、フォルダーコンテンツ テーブルは、列セットへのメッセージ クラス固有のプロパティの追加をサポートする必要があります。
  
クライアントは [、IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) メソッドを呼び出すことによって、フォルダーコンテンツ テーブルの既定の並べ替え順序を保存できます。 呼び出RECURSIVE_SORTフラグが指定されている場合、並べ替え順序を作成して、フォルダー内のすべてのサブフォルダーに適用できます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

