---
title: リモート ビューアーを作成します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 554f98f7bda8c6616ce06b86142213c18bff1f69
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804242"
---
# <a name="writing-a-remote-viewer"></a>リモート ビューアーを作成します。

**適用対象**: Outlook 
  
リモート ビューアーは、別のコンピューターに格納されているメッセージに対するアクセスの制御を提供するクライアント アプリケーションのウィンドウです。 この制御されたアクセスが低速の通信リンクを動作可能性があります。 ユーザーがフォルダーを開くたびに使用可能なメッセージの完全な選択範囲を取得するのではなくリモート ビューアーは最初のヘッダーだけを表示します。 ユーザーがヘッダーからを選択し、完全に表示するメッセージのうち。 ビューアーがリモート クライアントには、これまでダウンロードされる前にメッセージを削除するのには、ユーザーを許可できます。 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>リモートで格納されているメッセージのヘッダーを取得するには
  
1. ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。 
    
2. 状態テーブルを持つ行のみを制限する[IMAPITable::Restrict](imapitable-restrict.md)を呼び出して、 **PR\_リソース\_型**([PidTagResourceType](pidtagresourcetype-canonical-property.md))] 列には、MAPI 設定\_トランスポート\_プロバイダーです。 
    
3. ステータス テーブルに、次の列を含めるには、 [IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出します。 
   - **PR\_エントリ ID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR\_リソース\_メソッド**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR\_リソース\_タイプ**、 **PR\_プロバイダー\_表示**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR\_ステータス\_コード**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))。
    
4. 状態テーブル内のすべての行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。 
    
5. [IMAPISession::OpenEntry](imapisession-openentry.md)への呼び出しで、表の行ごとにエントリの識別子を渡します。 このインターフェイスが MAPI スプーラーでのプロセスのコンテキストからクライアントのプロセスのコンテキストにマーシャ リングするため、インタ フェースのアドレス帳またはメッセージから取得した通常とは異なり、プロバイダーを格納、マルチ スレッドは、多くの重要性についての問題します。 
    
6. リモート フォルダーを取得するのには、インターフェイス識別子として IID_IMAPIFolder を渡すことの状態のオブジェクトの[IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx)メソッドを呼び出します。 リモート フォルダーは、フォルダーの完全な実装ではありません。フォルダーのメソッドおよびプロパティのサブセットのみがサポートされています。 必須のメソッドでは、 [IMAPIProp::GetProps](imapiprop-getprops.md)のいずれかには、次のプロパティの取得がサポートされています。
    
    |||
    |:-----|:-----|
    |**PR\_アクセス**([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL**([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT**([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR\_サブフォルダー** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    リモート フォルダーには、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)、および[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)メソッドもサポートしなければなりません。 リモート フォルダーの内容のテーブルには、通常、次の列をサポートします。 
        
    |||
    |:-----|:-----|
    |**PR\_表示\_に**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR\_エントリ ID** <br/> |
    |**PR\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS**([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. 転送のオプションのいずれかが選択するトランスポート プロバイダーの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドの最初の時間を呼び出します。 表示されるユーザー ・ インタ フェースを使用するのには、SHOW_XP_SSESSION_UI フラグと REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE のいずれかの処理のフラグを設定してください。 
    
   > [!NOTE]
   > 特定のメッセージ ヘッダーをダウンロードまたは削除をマークするには、クライアントは[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)を呼び出すし、MSGSTATUS_REMOTE_DOWNLOAD または MSGSTATUS_REMOTE_DELETE のいずれかのフラグを設定します。 
  

