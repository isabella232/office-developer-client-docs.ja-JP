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
# <a name="tables-and-memory-usage"></a><span data-ttu-id="bf02c-103">テーブルとメモリの使用状況</span><span class="sxs-lookup"><span data-stu-id="bf02c-103">Tables and memory usage</span></span>

<span data-ttu-id="bf02c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf02c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf02c-105">テーブルからデータを取得することに関連する重要な問題は、メモリ使用量です。</span><span class="sxs-lookup"><span data-stu-id="bf02c-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="bf02c-106">使用可能なメモリが不足していると、 [IMAPITable:: QueryRows](imapitable-queryrows.md)および[hrqueryallrows](hrqueryallrows.md)は失敗し、目的の行数よりも小さい値が返されます。</span><span class="sxs-lookup"><span data-stu-id="bf02c-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="bf02c-107">テーブルデータを取得するために使用するメソッドまたは関数を決定する方法は、テーブルをメモリに収めることが予想されるかどうか、また失敗した場合にはエラーが許容できるかどうかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="bf02c-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="bf02c-108">メモリに格納されるデータ量を一度に決定することは常に容易ではないため、MAPI では、クライアントアプリケーションまたはサービスプロバイダーが従う必要のあるいくつかの基本的なガイドラインが提供されています。</span><span class="sxs-lookup"><span data-stu-id="bf02c-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="bf02c-109">特定のテーブルの実装と、基になるデータの格納方法に基づいて、常に例外があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bf02c-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="bf02c-110">次のガイドラインを使用して、テーブルのメモリ使用量を評価できます。</span><span class="sxs-lookup"><span data-stu-id="bf02c-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="bf02c-111">不定期に作業することができるクライアントは、メガバイト範囲のメモリ使用量を設定することができ、テーブル全体をメモリに読み込む際に問題が発生しないことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="bf02c-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="bf02c-112">制限は、テーブルのメモリ使用量に影響します。</span><span class="sxs-lookup"><span data-stu-id="bf02c-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="bf02c-113">contents テーブルのような大量の行を含む、厳しく制限されたテーブルは、通常、制限のない大きなテーブルではメモリに収めることができます。</span><span class="sxs-lookup"><span data-stu-id="bf02c-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="bf02c-114">状態、プロファイル、メッセージサービス、プロバイダー、およびメッセージストアテーブルなど、MAPI が所有するいくつかのテーブルは、通常、メモリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="bf02c-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="bf02c-115">これらは一般的に小さな表です。</span><span class="sxs-lookup"><span data-stu-id="bf02c-115">These are generally small tables.</span></span> <span data-ttu-id="bf02c-116">ただし、例外があります。</span><span class="sxs-lookup"><span data-stu-id="bf02c-116">However, there are exceptions.</span></span> <span data-ttu-id="bf02c-117">たとえば、サーバーベースのプロファイルプロバイダーでは、格納できないより大きなプロファイルテーブルが生成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="bf02c-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="bf02c-118">問題なくメモリに入りきるテーブルのすべての行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出して、最大行数を0に設定します。</span><span class="sxs-lookup"><span data-stu-id="bf02c-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="bf02c-119">メモリに格納されていない可能性がある行をすべて取得するには、エラーが発生します。最大行数を指定して**hrqueryallrows**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bf02c-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="bf02c-120">行数の最大数は、必要な最小行数よりも大きい値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf02c-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="bf02c-121">クライアントが300の行テーブルから50行以上の行にアクセスする必要がある場合は、行の最大数を少なくとも51に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf02c-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="bf02c-122">メモリに格納することが想定されていないすべての行をテーブルから取得するには、次のコードサンプルに示すように、比較的小さな行数のループで[IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bf02c-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="bf02c-123">このループが完了し、テーブル内のすべての行が処理され、 _cRows_が0の場合、通常、カーソルの位置は表の一番下になります。</span><span class="sxs-lookup"><span data-stu-id="bf02c-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf02c-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf02c-124">See also</span></span>

- [<span data-ttu-id="bf02c-125">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="bf02c-125">MAPI Tables</span></span>](mapi-tables.md)

