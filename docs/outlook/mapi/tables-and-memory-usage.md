---
title: テーブルとメモリの使用状況
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436861"
---
# <a name="tables-and-memory-usage"></a>テーブルとメモリの使用状況

**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルからデータを取得する際の重要な問題は、メモリ使用量です。 使用可能なメモリが不足すると [、IMAPITable::QueryRows](imapitable-queryrows.md) と [HrQueryAllRows](hrqueryallrows.md) が失敗し、必要な行数よりも少ない値が返される可能性があります。 テーブル データの取得に使用するメソッドまたは関数の決定は、テーブルがメモリに収まると予想できるかどうかと、テーブルに収まらない場合はエラーが許容されるかどうかによって異なります。 
  
一度にメモリに収まるデータ量を特定するのは必ずしも容易ではないので、MAPI には、クライアント アプリケーションまたはサービス プロバイダーが従う基本的なガイドラインがいくつか示されています。 特定のテーブルの実装と基になるデータの格納方法に基づいて、常に例外が発生します。
  
次のガイドラインを使用して、テーブルのメモリ使用量を評価できます。
  
- メガバイト範囲のワーキング セット のメモリ使用量を許容できるクライアントで、テーブル全体をメモリに読み込む際に問題が発生しない可能性があります。 
    
- 制限は、テーブルのメモリ使用量に影響します。 コンテンツ テーブルなど、多数の行を含む厳しく制限されたテーブルはメモリに収まると予想され、制限のない大きなテーブルは通常は使用できません。 
    
- 状態、プロファイル、メッセージ サービス、プロバイダー、メッセージ ストア テーブルなど、MAPI が所有するテーブルの中には、通常、メモリに収まるものがあります。 これらは一般的に小さいテーブルです。 ただし、例外があります。 たとえば、サーバー ベースのプロファイル プロバイダーは、収まらない大きなプロファイル テーブルを生成する場合があります。
    
問題がないメモリに収まるテーブルからすべての行を取得するには [、HrQueryAllRows](hrqueryallrows.md)を呼び出し、行の最大数を 0 に設定します。
  
メモリに収まらない可能性があるテーブルからすべての行を取得し、エラーを生成するには、最大行数を指定して **HrQueryAllRows** を呼び出します。 行の最大数は、必要な最小行数より大きい数に設定する必要があります。 クライアントが 300 行テーブルから少なくとも 50 行にアクセスする必要がある場合は、行の最大数を少なくとも 51 に設定する必要があります。 
  
メモリに収まるとは思わないテーブルからすべての行を取得するには、次のコード サンプルに示すように、比較的小さい行数のループで [IMAPITable::QueryRows](imapitable-queryrows.md) を呼び出します。 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

このループが完了し、テーブル内のすべての行が処理され  _、cRows_ が 0 の場合、カーソルの位置は通常、テーブルの下部になります。 
  
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

