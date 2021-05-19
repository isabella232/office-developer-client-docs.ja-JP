---
title: Folder-Associated情報テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426416"
---
# <a name="folder-associated-information-tables"></a>Folder-Associated情報テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI では、関連する情報MAPI_ASSOCIATED処理するときに使用するさまざまな MAPI コンポーネントのフラグを定義します。 メッセージ ストア内の各フォルダーには、標準コンテンツ テーブルと共に関連付けられたコンテンツ テーブルが必要です。 クライアント アプリケーションは、フォームとビューを保持するために、フォルダーに関連付けられたコンテンツ テーブルに特別なメッセージを格納します。 実際、フォームとビューをサポートするには、メッセージ ストア プロバイダーが関連付けられたコンテンツ テーブルを実装する必要があります。
  
関連付けられたコンテンツ テーブルを実装するには、ストア プロバイダーが次の操作を行う必要があります。
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドで MAPI_ASSOCIATED フラグをサポートし、クライアント アプリケーションが標準コンテンツ テーブルの代わりにフォルダーの関連コンテンツ テーブルを取得できます。 
    
- [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドで MAPI_ASSOCIATED フラグをサポートし、クライアント アプリケーションがフォルダーの関連付けられたコンテンツ テーブルにメッセージを追加できます。 
    
- フォルダー オブジェクトの MAPI_ACCESS_CREATE_ASSOCIATED **(** [PidTagAccess](pidtagaccess-canonical-property.md)) プロパティPR_ACCESSビットを設定します。
    
- [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)メソッドでDEL_ASSOCIATEDフラグをサポートします。 
    
- 関連付けられたMSGFLAG_ASSOCIATED内のメッセージの PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティのビットを設定します。
    
- フォルダーのプロパティ **PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents) プロパティ (PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)を公開し、そのプロパティに応答します。
    
- フォルダーの PR_ASSOC_CONTENT_COUNT ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) プロパティを維持します。
    
メッセージ ストア プロバイダーが関連付けられたコンテンツ **テーブルを** サポートするかどうかをPR_STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティにビットはありません。 メッセージ ストア プロバイダーがそれらをサポートしていない場合は、クライアント アプリケーションが MAPI_E_NO_SUPPORT フラグを指定して上記のメソッドを呼び出した場合に、MAPI_ASSOCIATED を返す必要があります。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

