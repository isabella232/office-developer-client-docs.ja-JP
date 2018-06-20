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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 64a64029c3507d9ac4b520076a44e23170dd9bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800508"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder: IMAPIContainer

  
  
**適用されます**: Outlook 
  
フォルダー内のメッセージとサブフォルダーに対して操作を実行します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |フォルダー オブジェクト  <br/> |
|によって実装されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションと MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFolder  <br/> |
|ポインターの型。  <br/> |LPMAPIFOLDER  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[メイル](imapifolder-createmessage.md) <br/> |新しいメッセージを作成します。  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |1 つまたは複数のメッセージを移動またはコピーします。  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |1 つまたは複数のメッセージを削除します。  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |新しいサブフォルダーを作成します。  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |サブフォルダーを移動またはコピーします。  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |サブフォルダーを削除します。  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |設定または、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティに 1 つまたは複数のフォルダーのメッセージでは、MSGFLAG_READ フラグをクリアし、リードのレポートの送信を管理します。  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |特定のフォルダー内のメッセージに関連付けられているステータスを取得します。  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |メッセージに関連付けられているステータスを設定します。  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |フォルダーの内容のテーブルの既定の並べ替え順序を設定します。  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |フォルダー自体を削除することがなく、フォルダーからすべてのメッセージとサブフォルダーを削除します。  <br/> |
   
|**必要なプロパティ**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

