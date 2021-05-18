---
title: 受信トレイ フォルダーのトラバー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406557"
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
    

