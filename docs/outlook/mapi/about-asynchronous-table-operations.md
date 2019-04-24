---
title: 非同期テーブル操作について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329021"
---
# <a name="about-asynchronous-table-operations"></a>非同期テーブル操作について
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
**IMAPITable**インターフェイスには、非同期操作を制御するための3つのメソッドを非同期で操作する3つのメソッドが含まれています。 次の表に、これらのメソッドを示します。 
  
|**非同期操作**|**非同期コントロールメソッド**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**テーブルの種類と現在の操作に関する状態情報を取得するには**
  
- 呼び出し[IMAPITable:: GetStatus](imapitable-getstatus.md)。 **GetStatus**では、テーブルのユーザーは、テーブルが静的または動的かどうか、操作が進行中であるか、完了したか、および完了した操作でエラーが発生したかどうかを判断できます。 たとえば、クライアントが時間がかかりすぎているために並べ替え操作を取り消す必要がある場合、最初に**GetStatus**を呼び出して、実際には並べ替え操作が現在処理中であるかどうかを判断できます。 その後、クライアントは[IMAPITable:: Abort](imapitable-abort.md)を呼び出して、これを停止できます。 
    
**非同期タスクが完了するまでアクティビティを中断するには**
  
- 呼び出し[IMAPITable:: waitforcompletion](imapitable-waitforcompletion.md)。 **waitforcompletion**を呼び出すことにより、タスクを中断することなく完了できます。 
    
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

