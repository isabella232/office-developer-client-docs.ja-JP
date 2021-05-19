---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424239"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダー内のメッセージとサブフォルダーに対して操作を実行します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォルダー オブジェクト  <br/> |
|実装元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションと MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFolder  <br/> |
|ポインターの種類:  <br/> |LPMAPIFOLDER  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |新しいメッセージを作成します。  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |1 つ以上のメッセージをコピーまたは移動します。  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |1 つ以上のメッセージを削除します。  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |新しいサブフォルダーを作成します。  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |サブフォルダーをコピーまたは移動します。  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |サブフォルダーを削除します。  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |**1** つ以上のフォルダーのメッセージの PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、読み取りレポートの送信を管理します。  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |特定のフォルダー内のメッセージに関連付けられている状態を取得します。  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |メッセージに関連付けられた状態を設定します。  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |フォルダーのコンテンツ テーブルの既定の並べ替え順序を設定します。  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |フォルダー自体を削除せずに、フォルダーからすべてのメッセージとサブフォルダーを削除します。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

