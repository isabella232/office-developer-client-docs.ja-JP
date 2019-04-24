---
title: リモート ビューアーの作成
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325663"
---
# <a name="writing-a-remote-viewer"></a>リモート ビューアーの作成

**適用対象**: Outlook 2013 | Outlook 2016 
  
リモートビューアーは、別のコンピューターに格納されているメッセージへの制御されたアクセスを提供するクライアントアプリケーションのウィンドウです。 この制御されたアクセスは、低速通信リンク上で動作する可能性があります。 ユーザーがフォルダーを開くたびに、使用可能なメッセージの完全な選択を取得するのではなく、最初にリモートビューアーにはヘッダーのみが表示されます。 ユーザーは、メッセージが完全に表示されるヘッダーから選択します。 リモートビューアークライアントは、ユーザーがダウンロードされる前にメッセージを削除できるようにすることができます。 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>リモートで保存されたメッセージのヘッダーを取得するには
  
1. 呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。 
    
2. 呼び出し[IMAPITable::](imapitable-restrict.md) [状態] テーブルを [ **PR\_\_RESOURCE TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))] 列が MAPI\_TRANSPORT\_PROVIDER に設定されている行だけに制限します。 
    
3. 次の列を状態テーブルに含めるには、 [IMAPITable:: SetColumns](imapitable-setcolumns.md)を呼び出します。 
   - **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR\_リソース\_メソッド**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **pr\_リソース\_の種類**、 **\_pr\_プロバイダーの表示**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR\_状態\_コード**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))。
    
4. [hrqueryallrows](hrqueryallrows.md)を呼び出して、状態テーブル内のすべての行を取得します。 
    
5. [imapisession:: openentry](imapisession-openentry.md)の呼び出しで、table 内の各行のエントリ識別子を渡します。 このインターフェイスは、MAPI スプーラーのプロセスコンテキストからクライアントのプロセスコンテキストにマーシャリングされるため、一般的にアドレス帳やメッセージストアプロバイダーから取得されるインターフェイスとは異なり、マルチスレッドに関する問題の方が重要です。 
    
6. 状態オブジェクトの[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx)メソッドを呼び出して、インターフェイス識別子として IID_IMAPIFolder を渡し、リモートフォルダーを取得します。 リモートフォルダーは、完全なフォルダーの実装ではありません。フォルダーのメソッドとプロパティのサブセットのみがサポートされています。 必要なメソッドの1つである[imapiprop:: GetProps](imapiprop-getprops.md)は、次のプロパティの取得をサポートしています。
    
    |||
    |:-----|:-----|
    |**PR\_アクセス**([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL**([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT**([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR\_サブフォルダー** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    リモートフォルダーは、 [imapiprop:: getproplist](imapiprop-getproplist.md)、 [IMAPIContainer:: getproplist](imapicontainer-getcontentstable.md)、 [imapiprop:: setmessagestatus](imapifolder-setmessagestatus.md)の各メソッドもサポートしている必要があります。 リモートフォルダーの内容の表は、通常、次の列をサポートしています。 
        
    |||
    |:-----|:-----|
    |**PR\_表示\_** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR\_ENTRYID** <br/> |
    |**PR\_hasattach** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS**([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. 転送オプションの1つを最初に選択したときに、トランスポートプロバイダーの[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを呼び出します。 ユーザーインターフェイスを表示できるようにするには、REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE のプロセスフラグだけでなく、SHOW_XP_SSESSION_UI フラグを設定する必要があります。 
    
   > [!NOTE]
   > ダウンロードまたは削除のために特定のメッセージヘッダーをマークするため、クライアントは[imapifolder:: setmessagestatus](imapifolder-setmessagestatus.md)を呼び出し、MSGSTATUS_REMOTE_DOWNLOAD フラグまたは MSGSTATUS_REMOTE_DELETE フラグのどちらかを設定します。 
  

