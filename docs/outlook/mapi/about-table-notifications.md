---
title: テーブル通知について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d6fd49e1a004202e0de02e262f6977ca8a07019d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571942"
---
# <a name="about-table-notifications"></a>テーブル通知について

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントは、多くの場合については、オブジェクトから直接通知を受け取るに登録する代わりにオブジェクトへの変更の通知をテーブルに依存しています。 通知の送信が発生する一般的な変更には、追加、削除、または行と、重大なエラーの修正が含まれます。 通知が到着したとき、クライアントは、テーブルを再ロードするのには別の呼び出しを行うかどうかを判断できます。 
  
テーブルの通知は非同期であるためより小さく単純な処理通知を行うことができるいくつかの問題があります。
  
- [TABLE_NOTIFICATION](table_notification.md)構造体に渡されるデータは、テーブルの最新の状態を表さないことがあります。 たとえば、クライアントは、メッセージに変更を加えるし、それを削除します。 メッセージ ストア プロバイダーがメッセージに含まれているコンテンツのテーブルを実装する 2 つの通知を送信する: TABLE_ROW_MODIFIED のイベントの後に、TABLE_ROW_DELETED イベントです。 によってどのようにメッセージ ストア プロバイダーは、通知を時間、クライアントは、行の削除後 TABLE_ROW_MODIFIED 通知を受け取る可能性があります。 
    
- 設定、通知に含まれる列は、テーブルの現在の列のセットとは異なる場合があります。 MAPI では、通知の列のセットが、通知が生成された時点で有効であった列セットと一致する必要があります。 クライアントが任意の時点を設定する列を変更するのには[IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出すための可能性があるため-通知した場合を含め、2 つの列セットを同期できない可能性があります。 
    
- ビューの一部である行のテーブルの通知を送信のみです。 制限があるため、ビューからの行が除外されている場合、またはテーブルが折りたたまれた状態であるため、通知が送信されますない場合はその行が変更されました。 また、カテゴリの状態の変更をクライアントに通知する通知は送信されません。
    
クライアントがありますしないすべてのテーブルが TABLE_SORT_DONE の通知をサポートしでこの条件を処理するために準備する必要。
  
1. 同期する並べ替えを強制します。
    
2. [IMAPITable::SortTable](imapitable-sorttable.md)が返されるときに、テーブルの行を再読み込みします。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

