---
title: 受信トレイ フォルダーを通過します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 87fcde5a28a30f08bc2fd5f28fb692a4b4251fbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804139"
---
# <a name="traversing-the-inbox-folder"></a>受信トレイ フォルダーを通過します。

  
  
**適用されます**: Outlook 
  
 **すべての受信トレイのメッセージを順番に表示**
  
1. 受信トレイのエントリ id を取得するために[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出します。 
    
2. 受信トレイを開くには、 **IMAPIFolder::OpenEntry**を呼び出します。 
    
3. コンテンツ テーブルを取得するために、受信トレイの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出します。 
    
4. 内容**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) に設定する列および必要なその他の任意の列を制限するテーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出します。 
    
5. 行のグループを取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。 
    
6. まで、内容のテーブルには不要になったすべての行があります。
    
1. 各行からのエントリの識別子によって表されるメッセージを開くには、 [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
    
2. ローカル**IMessage**インターフェイス ポインターには、 _lppUnk_パラメーターを割り当てます。 
    
3. メッセージのプロパティを操作します。
    
4. _LppUnk_パラメーターで指定されたポインターを解放します。 
    
5. 行の次のグループを取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。 
    
7. コンテンツ テーブルを解放します。
    

