---
title: フォルダー受信テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573181"
---
# <a name="receive-folder-tables"></a>フォルダー受信テーブル

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
受信フォルダー テーブルには、メッセージ ストアの受信フォルダーとして指定されているすべてのフォルダーの情報が含まれています。 受信フォルダーは、特定のメッセージ クラスの着信メッセージが配置されているフォルダーです。 メッセージ ストア プロバイダーの実装には、フォルダーのテーブルが表示され、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドを呼び出すことによって、クライアント アプリケーションを使用します。 
  
必要な列セットを次のプロパティには、フォルダーのテーブルに表示されます。
  
 **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

