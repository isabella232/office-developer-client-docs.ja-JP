---
title: 受信トレイフォルダーのスキャン
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
# <a name="traversing-the-inbox-folder"></a>受信トレイフォルダーのスキャン

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **受信トレイ内のすべてのメッセージを巡回するには**
  
1. [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を呼び出して、受信トレイのエントリ識別子を取得します。 
    
2. **imapifolder:: openentry**を呼び出して、受信トレイを開きます。 
    
3. 受信トレイの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出して、contents テーブルを取得します。 
    
4. コンテンツテーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列が**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) に設定され、その他の必要な列を制限します。 
    
5. 行のグループを取得するには、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。 
    
6. contents テーブルに行がなくなるまで、次のようになります。
    
1. [IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、各行からのエントリ id で表されるメッセージを開きます。 
    
2. _lppunk_パラメーターをローカルの**IMessage**インターフェイスポインターに割り当てます。 
    
3. メッセージのプロパティを操作します。
    
4. _lppunk_パラメーターで示されているポインターを解放します。 
    
5. 次の行グループを取得するには、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。 
    
7. 目次表を解放します。
    

