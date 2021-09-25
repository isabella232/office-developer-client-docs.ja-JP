---
title: フォルダー テーブルの受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2cf12e7e73ca55100fdb51d2d9cc1ba5d5a8b9bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609615"
---
# <a name="receive-folder-tables"></a>フォルダー テーブルの受信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信フォルダー テーブルには、メッセージ ストアの受信フォルダーとして指定されているすべてのフォルダーの情報が含まれています。 受信フォルダーは、特定のメッセージ クラスの受信メッセージが配置されるフォルダーです。 メッセージ ストア プロバイダーは受信フォルダー テーブルを実装し、クライアント アプリケーションは [、IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) メソッドを呼び出して使用します。 
  
次のプロパティは、受信フォルダー テーブルで必要な列セットを構成します。
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

