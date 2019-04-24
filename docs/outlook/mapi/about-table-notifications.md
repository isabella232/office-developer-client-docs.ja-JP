---
title: テーブル通知について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321841"
---
# <a name="about-table-notifications"></a>テーブル通知について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、オブジェクトから直接通知を受け取るように登録するのではなく、オブジェクトに対する変更を知るために table 通知に依存しています。 通知が送信される一般的な変更には、行の追加、削除、または変更、および重大なエラーがあります。 通知が到着すると、クライアントはテーブルを再読み込みするために別の呼び出しを行うかどうかを判断できます。 
  
テーブル通知は非同期であるため、簡単な通知を処理できない問題がいくつかあります。
  
- [TABLE_NOTIFICATION](table_notification.md)構造体で渡されるデータは、テーブルの最新の状態を表していない場合があります。 たとえば、クライアントがメッセージに変更を加えた後、それを削除する場合があります。 メッセージを含むコンテンツテーブルを実装するメッセージストアプロバイダーは、2つの通知を送信します。 TABLE_ROW_MODIFIED イベントの後に TABLE_ROW_DELETED イベントが続きます。 メッセージストアプロバイダーの通知方法によっては、クライアントは行の削除後に TABLE_ROW_MODIFIED 通知を受け取ることがあります。 
    
- 通知に含まれる列セットは、テーブルの現在の列セットと異なる場合があります。 MAPI では、通知の列セットが通知が生成されたときに有効になっていた列セットと一致している必要があります。 クライアントは[IMAPITable:: SetColumns](imapitable-setcolumns.md)を呼び出すことができるので、いつでも列セットを変更することができます。これは、通知後に2つの列セットが同期されない場合があります。 
    
- テーブル通知は、ビューの一部である行に対してのみ送信されます。 つまり、制限によって、またはテーブルが折りたたまれた状態であるために、ある行がビューから除外されている場合、その行が変更されても通知は送信されません。 また、カテゴリ状態の変更についてクライアントに通知する通知は送信されません。
    
クライアントは、すべてのテーブルが TABLE_SORT_DONE 通知をサポートしているわけではなく、次のようにしてこの条件を処理できるようにする必要があることに注意してください。
  
1. 強制的に並べ替えを同期させます。
    
2. [IMAPITable:: sorttable](imapitable-sorttable.md)から返されるときに、テーブルの行を再読み込みします。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

