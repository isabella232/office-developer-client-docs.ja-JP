---
title: 情報のフォルダーに関連付けられているテーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 09cac591aac9d266571348531e378974b86a3a9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800088"
---
# <a name="folder-associated-information-tables"></a>情報のフォルダーに関連付けられているテーブル

  
  
**適用されます**: Outlook 
  
MAPI では、関連する情報のテーブルを処理するときに使用する各種の MAPI コンポーネントの MAPI_ASSOCIATED フラグを定義します。 メッセージ ・ ストア内の各フォルダーには、標準的な内容のテーブルと、関連する内容のテーブルが必要です。 クライアント アプリケーションでは、フォームとビューを保持するためにフォルダーの内容が関連付けられているテーブルに特別なメッセージを保存します。 実際には、フォームとビューをサポートするため、メッセージ ストア プロバイダーは、関連付けられている内容のテーブルを実装しなければなりません。
  
コンテンツが関連付けられているテーブルを実装するには、ストア プロバイダーは、次の。
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドで MAPI_ASSOCIATED フラグをサポートし、ため、クライアント アプリケーションは、標準的な内容のテーブルではなく、フォルダーの内容が関連付けられているテーブルを取得できます。 
    
- クライアント アプリケーションは、フォルダーの内容が関連付けられているテーブルにメッセージを追加できるように、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドで MAPI_ASSOCIATED フラグをサポートします。 
    
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) のプロパティのフォルダー オブジェクトに MAPI_ACCESS_CREATE_ASSOCIATED ビットを設定します。
    
- [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)メソッドで、DEL_ASSOCIATED フラグをサポートします。 
    
- MSGFLAG_ASSOCIATED の**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) は、関連付けられているコンテンツ」テーブル内のメッセージのビットを設定します。
    
- 公開し、フォルダーの**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) のプロパティに対応します。
    
- フォルダーの**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) のプロパティを保持します。
    
メッセージ ストア プロバイダーが関連付けられている内容のテーブルをサポートしているかどうかを示すために**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティでは、ビットはありません。 メッセージ ストア プロバイダーではサポートしていない場合、クライアント アプリケーションでは、MAPI_ASSOCIATED フラグを使用して上記の方法のいずれかを呼び出すと、MAPI_E_NO_SUPPORT を返す必要があります。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

