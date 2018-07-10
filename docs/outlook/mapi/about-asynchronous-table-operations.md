---
title: 非同期テーブルの操作について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799595"
---
# <a name="about-asynchronous-table-operations"></a>非同期テーブルの操作について
 
**適用されます**: Outlook 
  
**IMAPITable**インターフェイスには、非同期的に動作する 3 つのメソッドと非同期操作を制御するための 3 つの方法が含まれています。 次の表に、これらのメソッドを示します。 
  
|**非同期操作**|**非同期制御方式**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**テーブルの種類と現在の操作に関するステータス情報を取得するには**
  
- [IMAPITable::GetStatus](imapitable-getstatus.md)を呼び出します。 **GetStatus**とテーブルのユーザーがかどうか、テーブルは、静的または動的な場合は、操作が進行中または完了すると場合と、完了した操作から、エラーが発生したかどうかを確認できます。 などの場合は、クライアントでは、あまり時間がかかるために、並べ替え操作をキャンセルする必要がある、クライアント最初を呼び出せるかどうか、実際には、並べ替え操作は、現在の処理を決定するのには、 **GetStatus** 。 クライアントはそれを停止するのには[IMAPITable::Abort](imapitable-abort.md)を呼び出すことができます。 
    
**非同期タスクが完了するまで活動を中断するのには**
  
- [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)を呼び出します。 **WaitForCompletion**を呼び出すことには、タスクを中断することがなく完了することができます。 
    
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)
