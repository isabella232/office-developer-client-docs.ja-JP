---
title: リモート ビューアーの作成
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325663"
---
# <a name="writing-a-remote-viewer"></a>リモート ビューアーの作成

**適用対象**: Outlook 2013 | Outlook 2016 
  
リモート ビューアーは、別のコンピューターに保存されているメッセージへの制御されたアクセスを提供するクライアント アプリケーションのウィンドウです。 この制御されたアクセスは、低速の通信リンクで動作する可能性があります。 ユーザーがフォルダーを開くごとに使用可能なメッセージの完全な選択を取得するのではなく、リモート ビューアーは最初にヘッダーのみを表示します。 次に、ヘッダーから、表示するメッセージを完全に選択します。 リモート ビューアー クライアントは、ユーザーがダウンロードされる前にメッセージを削除できます。 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>リモートで保存されているメッセージのヘッダーを取得するには
  
1. [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。 
    
2. [IMAPITable::Restrict](imapitable-restrict.md)を呼び出して、状態テーブルを **、PR \_ RESOURCE TYPE \_** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列が MAPI TRANSPORT PROVIDER に設定されている行にのみ \_ 制限 \_ します。 
    
3. [IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出して、状態テーブルに次の列を含める。 
   - **PR \_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR \_RESOURCE \_ メソッド** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR \_RESOURCE \_ 型**、 **PR PROVIDER \_ \_ DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR \_STATUS \_ CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))。
    
4. [HrQueryAllRows を呼](hrqueryallrows.md)び出して、状態テーブル内のすべての行を取得します。 
    
5. [IMAPISession::OpenEntry](imapisession-openentry.md)への呼び出しで、テーブル内の各行のエントリ識別子を渡します。 このインターフェイスは、MAPI スプーラーのプロセス コンテキストからクライアントのプロセス コンテキストにマーシャリングされます 。アドレス帳またはメッセージ ストア プロバイダーから通常取得されるインターフェイスとは異なり、マルチスレッド化に関する問題の方が重要です。 
    
6. status オブジェクトの [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) メソッドを呼び出し、IID_IMAPIFolderをインターフェイス識別子として渡して、リモート フォルダーを取得します。 リモート フォルダーは完全なフォルダーの実装ではありません。フォルダー メソッドとプロパティのサブセットのみをサポートします。 必要なメソッドの 1 つ [、IMAPIProp::GetProps](imapiprop-getprops.md)は、次のプロパティの取得をサポートします。
    
    |||
    |:-----|:-----|
    |**PR \_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR \_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    リモート フォルダーでは[、IMAPIProp::GetPropList、IMAPIContainer::GetContentsTable、IMAPIFolder::SetMessageStatus](imapicontainer-getcontentstable.md)メソッドもサポートする必要があります。 [](imapiprop-getproplist.md) [](imapifolder-setmessagestatus.md) リモート フォルダーのコンテンツ テーブルは、通常、次の列をサポートします。 
        
    |||
    |:-----|:-----|
    |**PR \_DISPLAY \_ TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR \_ ENTRYID** <br/> |
    |**PR \_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR \_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR \_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR \_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. トランスポート プロバイダーの [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドを初めて呼び出して、転送オプションの 1 つを選択します。 ユーザー インターフェイスREFRESH_XP_HEADER_CACHE表示PROCESS_XP_HEADER_CACHEするには、プロセス フラグまたはプロセス SHOW_XP_SSESSION_UI フラグを設定する必要があります。 
    
   > [!NOTE]
   > ダウンロードまたは削除用に特定のメッセージ ヘッダーをマークするために、クライアントは [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) を呼び出し、MSGSTATUS_REMOTE_DOWNLOAD フラグまたは MSGSTATUS_REMOTE_DELETE フラグを設定します。 
  

