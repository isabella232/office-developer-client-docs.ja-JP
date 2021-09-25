---
title: 受信トレイ フォルダーのトラバー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 82dfaf9a09a9dca5a29764aad0ee07363d133435
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624014"
---
# <a name="traversing-the-inbox-folder"></a>受信トレイ フォルダーのトラバー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **受信トレイ内のすべてのメッセージを循環するには**
  
1. 受信 [トレイのエントリ識別子を取得するには、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) を呼び出します。 
    
2. **IMAPIFolder::OpenEntry を呼び出して** 受信トレイを開きます。 
    
3. 受信トレイの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) メソッドを呼び出して、コンテンツ テーブルを取得します。 
    
4. **コンテンツ** テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) および必要なその他の列に制限します。 
    
5. [IMAPITable::QueryRows を呼び出して](imapitable-queryrows.md)、行のグループを取得します。 
    
6. コンテンツ テーブルに行がなくなるまで、次の処理を実行します。
    
1. [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出して、各行のエントリ識別子で表されるメッセージを開きます。 
    
2. _lppUnk パラメーターを_ ローカルの IMessage インターフェイス ポインター **に割り** 当てる。 
    
3. メッセージのプロパティを使用します。
    
4. _lppUnk_ パラメーターが指すポインターを離します。 
    
5. [IMAPITable::QueryRows を呼び出して](imapitable-queryrows.md)、次の行グループを取得します。 
    
7. コンテンツ テーブルを解放します。
    

