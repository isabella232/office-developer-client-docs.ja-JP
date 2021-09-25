---
title: テーブル通知について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b950f013451dbe7e716cdffa3303ccc6bfb23976
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572208"
---
# <a name="about-table-notifications"></a>テーブル通知について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、多くの場合、オブジェクトから直接通知を受信するために登録する代わりに、テーブル通知を使用してオブジェクトに対する変更を学習します。 通知の送信を引き起こす一般的な変更には、行の追加、削除、または変更、重大なエラーが含まれます。 通知が到着すると、クライアントはテーブルを再読み込みするために別の呼び出しを行うかどうかを決定できます。 
  
テーブル通知は非同期なので、通知の処理を簡単に行う可能性があるいくつかの問題があります。
  
- TABLE_NOTIFICATION構造で [渡されたデータ](table_notification.md) は、テーブルの最新の状態を表していない可能性があります。 たとえば、クライアントがメッセージに変更を行い、メッセージを削除する場合があります。 メッセージを含むコンテンツ テーブルを実装するメッセージ ストア プロバイダーは、TABLE_ROW_MODIFIED イベントとイベントの 2 つの通知TABLE_ROW_DELETEDします。 メッセージ ストア プロバイダーが通知を回す方法に応じて、クライアントは行の削除後にTABLE_ROW_MODIFIED通知を受け取る場合があります。 
    
- 通知に含まれる列セットは、テーブルの現在の列セットとは異なる場合があります。 MAPI では、通知列セットが、通知が生成された時点で有効だった列セットと一致する必要があります。 クライアントが [IMAPITable::SetColumns](imapitable-setcolumns.md) を呼び出して、通知後も含めていつでも列セットを変更できる可能性があるから、2 つの列セットは同期できない可能性があります。 
    
- テーブル通知は、ビューの一部である行にのみ送信されます。 つまり、制限のために行がビューから除外されている場合、またはテーブルが折りたたみ状態にある場合、その行が変更された場合は通知は送信されません。 また、カテゴリの状態の変更についてクライアントに通知する通知は送信されません。
    
クライアントは、すべてのテーブルが通知をサポートしているTABLE_SORT_DONE、次の方法でこの条件を処理する準備が必要です。
  
1. 並べ替えを同期に設定します。
    
2. [IMAPITable::SortTable が返された場合にテーブルの行を](imapitable-sorttable.md)再読み込みします。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

