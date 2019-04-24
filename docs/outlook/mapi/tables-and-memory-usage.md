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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320406"
---
# <a name="tables-and-memory-usage"></a>テーブルとメモリの使用状況

**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルからデータを取得することに関連する重要な問題は、メモリ使用量です。 使用可能なメモリが不足していると、 [IMAPITable:: QueryRows](imapitable-queryrows.md)および[hrqueryallrows](hrqueryallrows.md)は失敗し、目的の行数よりも小さい値が返されます。 テーブルデータを取得するために使用するメソッドまたは関数を決定する方法は、テーブルをメモリに収めることが予想されるかどうか、また失敗した場合にはエラーが許容できるかどうかによって決まります。 
  
メモリに格納されるデータ量を一度に決定することは常に容易ではないため、MAPI では、クライアントアプリケーションまたはサービスプロバイダーが従う必要のあるいくつかの基本的なガイドラインが提供されています。 特定のテーブルの実装と、基になるデータの格納方法に基づいて、常に例外があることに注意してください。
  
次のガイドラインを使用して、テーブルのメモリ使用量を評価できます。
  
- 不定期に作業することができるクライアントは、メガバイト範囲のメモリ使用量を設定することができ、テーブル全体をメモリに読み込む際に問題が発生しないことを前提としています。 
    
- 制限は、テーブルのメモリ使用量に影響します。 contents テーブルのような大量の行を含む、厳しく制限されたテーブルは、通常、制限のない大きなテーブルではメモリに収めることができます。 
    
- 状態、プロファイル、メッセージサービス、プロバイダー、およびメッセージストアテーブルなど、MAPI が所有するいくつかのテーブルは、通常、メモリに格納されます。 これらは一般的に小さな表です。 ただし、例外があります。 たとえば、サーバーベースのプロファイルプロバイダーでは、格納できないより大きなプロファイルテーブルが生成されることがあります。
    
問題なくメモリに入りきるテーブルのすべての行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出して、最大行数を0に設定します。
  
メモリに格納されていない可能性がある行をすべて取得するには、エラーが発生します。最大行数を指定して**hrqueryallrows**を呼び出します。 行数の最大数は、必要な最小行数よりも大きい値に設定する必要があります。 クライアントが300の行テーブルから50行以上の行にアクセスする必要がある場合は、行の最大数を少なくとも51に設定する必要があります。 
  
メモリに格納することが想定されていないすべての行をテーブルから取得するには、次のコードサンプルに示すように、比較的小さな行数のループで[IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。 
  
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

このループが完了し、テーブル内のすべての行が処理され、 _cRows_が0の場合、通常、カーソルの位置は表の一番下になります。 
  
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

