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
# <a name="tables-and-memory-usage"></a><span data-ttu-id="5c77a-103">テーブルとメモリの使用状況</span><span class="sxs-lookup"><span data-stu-id="5c77a-103">Tables and memory usage</span></span>

<span data-ttu-id="5c77a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c77a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c77a-105">テーブルからデータを取得する際の重要な問題は、メモリ使用量です。</span><span class="sxs-lookup"><span data-stu-id="5c77a-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="5c77a-106">使用可能なメモリが不足すると [、IMAPITable::QueryRows](imapitable-queryrows.md) と [HrQueryAllRows](hrqueryallrows.md) が失敗し、必要な行数よりも少ない値が返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="5c77a-107">テーブル データの取得に使用するメソッドまたは関数の決定は、テーブルがメモリに収まると予想できるかどうかと、テーブルに収まらない場合はエラーが許容されるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="5c77a-108">一度にメモリに収まるデータ量を特定するのは必ずしも容易ではないので、MAPI には、クライアント アプリケーションまたはサービス プロバイダーが従う基本的なガイドラインがいくつか示されています。</span><span class="sxs-lookup"><span data-stu-id="5c77a-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="5c77a-109">特定のテーブルの実装と基になるデータの格納方法に基づいて、常に例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="5c77a-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="5c77a-110">次のガイドラインを使用して、テーブルのメモリ使用量を評価できます。</span><span class="sxs-lookup"><span data-stu-id="5c77a-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="5c77a-111">メガバイト範囲のワーキング セット のメモリ使用量を許容できるクライアントで、テーブル全体をメモリに読み込む際に問題が発生しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="5c77a-112">制限は、テーブルのメモリ使用量に影響します。</span><span class="sxs-lookup"><span data-stu-id="5c77a-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="5c77a-113">コンテンツ テーブルなど、多数の行を含む厳しく制限されたテーブルはメモリに収まると予想され、制限のない大きなテーブルは通常は使用できません。</span><span class="sxs-lookup"><span data-stu-id="5c77a-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="5c77a-114">状態、プロファイル、メッセージ サービス、プロバイダー、メッセージ ストア テーブルなど、MAPI が所有するテーブルの中には、通常、メモリに収まるものがあります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="5c77a-115">これらは一般的に小さいテーブルです。</span><span class="sxs-lookup"><span data-stu-id="5c77a-115">These are generally small tables.</span></span> <span data-ttu-id="5c77a-116">ただし、例外があります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-116">However, there are exceptions.</span></span> <span data-ttu-id="5c77a-117">たとえば、サーバー ベースのプロファイル プロバイダーは、収まらない大きなプロファイル テーブルを生成する場合があります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="5c77a-118">問題がないメモリに収まるテーブルからすべての行を取得するには [、HrQueryAllRows](hrqueryallrows.md)を呼び出し、行の最大数を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="5c77a-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="5c77a-119">メモリに収まらない可能性があるテーブルからすべての行を取得し、エラーを生成するには、最大行数を指定して **HrQueryAllRows** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5c77a-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="5c77a-120">行の最大数は、必要な最小行数より大きい数に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="5c77a-121">クライアントが 300 行テーブルから少なくとも 50 行にアクセスする必要がある場合は、行の最大数を少なくとも 51 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="5c77a-122">メモリに収まるとは思わないテーブルからすべての行を取得するには、次のコード サンプルに示すように、比較的小さい行数のループで [IMAPITable::QueryRows](imapitable-queryrows.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5c77a-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="5c77a-123">このループが完了し、テーブル内のすべての行が処理され  _、cRows_ が 0 の場合、カーソルの位置は通常、テーブルの下部になります。</span><span class="sxs-lookup"><span data-stu-id="5c77a-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c77a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c77a-124">See also</span></span>

- [<span data-ttu-id="5c77a-125">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="5c77a-125">MAPI Tables</span></span>](mapi-tables.md)

