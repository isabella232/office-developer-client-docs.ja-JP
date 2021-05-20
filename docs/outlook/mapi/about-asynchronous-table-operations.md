---
title: 非同期テーブル操作について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439570"
---
# <a name="about-asynchronous-table-operations"></a>非同期テーブル操作について
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
**IMAPITable インターフェイスには**、非同期的に動作する 3 つのメソッドと、非同期操作を制御するための 3 つのメソッドが含まれています。 次の表に、これらのメソッドの一覧を示します。 
  
|**非同期操作**|**非同期制御メソッド**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**テーブルの種類と現在の操作に関する状態情報を取得するには**
  
- [IMAPITable::GetStatus を呼び出します](imapitable-getstatus.md)。 **GetStatus** を使用すると、テーブルのユーザーは、テーブルが静的か動的か、操作が進行中か完了したのか、完了した操作でエラーが発生したかどうかを判断できます。 たとえば、時間が長すぎるため、クライアントが並べ替え操作をキャンセルする必要がある場合、クライアントはまず **GetStatus** を呼び出して、実際に並べ替え操作が現在処理されているかどうかを判断できます。 その後、クライアントは [IMAPITable::Abort](imapitable-abort.md) を呼び出して停止できます。 
    
**非同期タスクが完了するまでアクティビティを中断するには**
  
- [IMAPITable::WaitForCompletion を呼び出します](imapitable-waitforcompletion.md)。 **WaitForCompletion を呼び出すことによって**、中断することなくタスクを完了できます。 
    
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

