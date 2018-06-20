---
title: テーブルとメモリ使用量
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804095"
---
# <a name="tables-and-memory-usage"></a>テーブルとメモリ使用量

**適用されます**: Outlook 
  
テーブルからデータを取得するのに接続されている重要な問題は、メモリ使用量です。 メモリ不足の発生することが[IMAPITable::QueryRows](imapitable-queryrows.md)と[HrQueryAllRows](hrqueryallrows.md)が失敗し、返す行の必要な数よりも少ない。 またはテーブルのデータを取得するために使用する関数を決定する際に依存テーブルがメモリに収まるように期待できるかどうか、できない場合は、失敗が許容される場合。 
  
簡単ではありません常にメモリに同時に適合するデータの量を決定する、ために、MAPI は、いくつかの基本的なガイドラインに従うには、クライアント アプリケーションまたはサービス プロバイダーを提供します。 特定のテーブルの実装と、基になるデータを格納する方法に基づいて、例外は常に注意してください。
  
テーブルのメモリ使用量を評価するためには、次のガイドラインを使用できます。
  
- 臨時ワーキング セット メモリの使用量メガバイトの範囲内で許容できるおよびそれらを使用すると見なすことができるクライアントには、メモリにテーブル全体を読み取り中に問題はありません。 
    
- 制限では、メモリのテーブルの使用状況に影響があります。 無制限の大規模なテーブルは通常できないときに、メモリに収まるように厳しく制限されるなど、内容のテーブルの行の数を広範なテーブルが期待できます。 
    
- メモリに収まる状態、プロファイル、メッセージ サービス、プロバイダー、およびメッセージ ストアのテーブルなど、MAPI によって所有されているテーブルのいくつかが通常です。 これらは、一般的に小さいテーブルです。 ただし、これには例外があります。 などのサーバー ベースのプロファイル プロバイダーは、適合することはできません大きいプロファイル表を生成する可能性があります。
    
問題なくメモリに収まるテーブルからすべての行を取得、 [HrQueryAllRows](hrqueryallrows.md)行の最大数を 0 に設定を呼び出します。
  
、エラーを生成する、メモリに収まらないことがありますか可能性がありますテーブルからすべての行を取得するには、行の最大数を指定する**HrQueryAllRows**を呼び出します。 行の最大数が設定数に必要な行の最小数を超える。 クライアントは、300 行のテーブルから 50 以上の行にアクセスする必要がある場合、は、51 以上に行の最大数を設定する必要があります。 
  
メモリに収まるように予期しないテーブルからすべての行を取得するには、コード例を次に示すように比較的少数の行の数では、ループに[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。 
  
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

このループが完了するし、テーブル内のすべての行が処理されたが、_カラス_はゼロをカーソルの位置は通常、テーブルの下部にあります。 
  
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

