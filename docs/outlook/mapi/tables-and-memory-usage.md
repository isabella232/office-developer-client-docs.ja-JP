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
# <a name="tables-and-memory-usage"></a><span data-ttu-id="16f1d-103">テーブルとメモリ使用量</span><span class="sxs-lookup"><span data-stu-id="16f1d-103">Tables and memory usage</span></span>

<span data-ttu-id="16f1d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16f1d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16f1d-105">テーブルからデータを取得するのに接続されている重要な問題は、メモリ使用量です。</span><span class="sxs-lookup"><span data-stu-id="16f1d-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="16f1d-106">メモリ不足の発生することが[IMAPITable::QueryRows](imapitable-queryrows.md)と[HrQueryAllRows](hrqueryallrows.md)が失敗し、返す行の必要な数よりも少ない。</span><span class="sxs-lookup"><span data-stu-id="16f1d-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="16f1d-107">またはテーブルのデータを取得するために使用する関数を決定する際に依存テーブルがメモリに収まるように期待できるかどうか、できない場合は、失敗が許容される場合。</span><span class="sxs-lookup"><span data-stu-id="16f1d-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="16f1d-108">簡単ではありません常にメモリに同時に適合するデータの量を決定する、ために、MAPI は、いくつかの基本的なガイドラインに従うには、クライアント アプリケーションまたはサービス プロバイダーを提供します。</span><span class="sxs-lookup"><span data-stu-id="16f1d-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="16f1d-109">特定のテーブルの実装と、基になるデータを格納する方法に基づいて、例外は常に注意してください。</span><span class="sxs-lookup"><span data-stu-id="16f1d-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="16f1d-110">テーブルのメモリ使用量を評価するためには、次のガイドラインを使用できます。</span><span class="sxs-lookup"><span data-stu-id="16f1d-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="16f1d-111">臨時ワーキング セット メモリの使用量メガバイトの範囲内で許容できるおよびそれらを使用すると見なすことができるクライアントには、メモリにテーブル全体を読み取り中に問題はありません。</span><span class="sxs-lookup"><span data-stu-id="16f1d-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="16f1d-112">制限では、メモリのテーブルの使用状況に影響があります。</span><span class="sxs-lookup"><span data-stu-id="16f1d-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="16f1d-113">無制限の大規模なテーブルは通常できないときに、メモリに収まるように厳しく制限されるなど、内容のテーブルの行の数を広範なテーブルが期待できます。</span><span class="sxs-lookup"><span data-stu-id="16f1d-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="16f1d-114">メモリに収まる状態、プロファイル、メッセージ サービス、プロバイダー、およびメッセージ ストアのテーブルなど、MAPI によって所有されているテーブルのいくつかが通常です。</span><span class="sxs-lookup"><span data-stu-id="16f1d-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="16f1d-115">これらは、一般的に小さいテーブルです。</span><span class="sxs-lookup"><span data-stu-id="16f1d-115">These are generally small tables.</span></span> <span data-ttu-id="16f1d-116">ただし、これには例外があります。</span><span class="sxs-lookup"><span data-stu-id="16f1d-116">However, there are exceptions.</span></span> <span data-ttu-id="16f1d-117">などのサーバー ベースのプロファイル プロバイダーは、適合することはできません大きいプロファイル表を生成する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="16f1d-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="16f1d-118">問題なくメモリに収まるテーブルからすべての行を取得、 [HrQueryAllRows](hrqueryallrows.md)行の最大数を 0 に設定を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16f1d-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="16f1d-119">、エラーを生成する、メモリに収まらないことがありますか可能性がありますテーブルからすべての行を取得するには、行の最大数を指定する**HrQueryAllRows**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16f1d-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="16f1d-120">行の最大数が設定数に必要な行の最小数を超える。</span><span class="sxs-lookup"><span data-stu-id="16f1d-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="16f1d-121">クライアントは、300 行のテーブルから 50 以上の行にアクセスする必要がある場合、は、51 以上に行の最大数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16f1d-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="16f1d-122">メモリに収まるように予期しないテーブルからすべての行を取得するには、コード例を次に示すように比較的少数の行の数では、ループに[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16f1d-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="16f1d-123">このループが完了するし、テーブル内のすべての行が処理されたが、_カラス_はゼロをカーソルの位置は通常、テーブルの下部にあります。</span><span class="sxs-lookup"><span data-stu-id="16f1d-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16f1d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="16f1d-124">See also</span></span>

- [<span data-ttu-id="16f1d-125">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="16f1d-125">MAPI Tables</span></span>](mapi-tables.md)

