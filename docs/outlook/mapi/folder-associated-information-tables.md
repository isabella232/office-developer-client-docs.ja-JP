---
title: フォルダーに関連付けられた情報テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342553"
---
# <a name="folder-associated-information-tables"></a>フォルダーに関連付けられた情報テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi は、関連する情報テーブルの処理に使用するさまざまな mapi コンポーネントの MAPI_ASSOCIATED フラグを定義します。 メッセージストア内の各フォルダーには、その標準コンテンツテーブルと共に、関連付けられた contents テーブルが含まれている必要があります。 クライアントアプリケーションは、フォームとビューを保持するために、フォルダーに関連付けられた contents テーブルに特別なメッセージを格納します。 実際に、フォームとビューをサポートするには、メッセージストアプロバイダーが関連するコンテンツテーブルを実装する必要があります。
  
関連するコンテンツテーブルを実装するには、ストアプロバイダーが次のことを行う必要があります。
  
- [IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドの MAPI_ASSOCIATED フラグをサポートすることにより、クライアントアプリケーションが、標準の contents テーブルではなく、フォルダーに関連付けられたコンテンツテーブルを取得できるようにします。 
    
- [imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドの MAPI_ASSOCIATED フラグをサポートすることにより、クライアントアプリケーションがフォルダーに関連付けられたコンテンツテーブルにメッセージを追加できるようにします。 
    
- folder オブジェクトの**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティで MAPI_ACCESS_CREATE_ASSOCIATED ビットを設定します。
    
- [imapifolder:: emptyfolder](imapifolder-emptyfolder.md)メソッドで DEL_ASSOCIATED フラグをサポートします。 
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_ASSOCIATED ビットを、関連付けられている contents テーブル内のメッセージに設定します。
    
- フォルダーの**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを公開して応答します。
    
- フォルダーの**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) プロパティを維持します。
    
**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティには、メッセージストアプロバイダーが関連付けられたコンテンツテーブルをサポートしているかどうかを示すビットはありません。 メッセージストアプロバイダーがサポートしていない場合は、クライアントアプリケーションが MAPI_ASSOCIATED フラグを使用して上記のいずれかのメソッドを呼び出すと、MAPI_E_NO_SUPPORT が返されます。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

