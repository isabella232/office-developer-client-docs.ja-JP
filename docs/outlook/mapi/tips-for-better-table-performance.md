---
title: テーブル パフォーマンス向上のためのヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412514"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="93501-103">テーブル パフォーマンス向上のためのヒント</span><span class="sxs-lookup"><span data-stu-id="93501-103">Tips for better table performance</span></span>
  
<span data-ttu-id="93501-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93501-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93501-105">テーブル操作の多くは時間がかかる可能性があり、進行状況を示す方法はないので、パフォーマンスを向上するために次の手法を使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="93501-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="93501-106">**[IMAPITable を作成する : IUnknown 呼](imapitableiunknown.md)び出しを正しい順序で行う**</span><span class="sxs-lookup"><span data-stu-id="93501-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="93501-107">クライアントとサービス プロバイダーは、さまざまな方法でテーブルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93501-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="93501-108">既定の列セットと並べ替え順序を使用して、テーブルを開き、すべての行のデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="93501-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="93501-109">または、列セットを変更したり、並べ替え順序を変更したり、テーブルの範囲を絞り込む制限を設定したりして、テーブルの既定のビューを変更できます。</span><span class="sxs-lookup"><span data-stu-id="93501-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="93501-110">データを取得する前に 1 つ以上の操作を実行するテーブル ユーザーは、次の順序で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93501-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="93501-111">[IMAPITable::SetColumns を使用して列セットを定義します](imapitable-setcolumns.md)。</span><span class="sxs-lookup"><span data-stu-id="93501-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="93501-112">[IMAPITable::Restrict を使用して制限を設定します](imapitable-restrict.md)。</span><span class="sxs-lookup"><span data-stu-id="93501-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="93501-113">[IMAPITable::SortTable を使用して並べ替え順序を定義します](imapitable-sorttable.md)。</span><span class="sxs-lookup"><span data-stu-id="93501-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="93501-114">この順序でこれらのタスクを実行すると、並べ替える行と列の数が制限され、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="93501-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="93501-115">**可能であれば、TBL_BATCHフラグを使用して操作を遅延する**</span><span class="sxs-lookup"><span data-stu-id="93501-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="93501-116">メソッドに TBL BATCH フラグを設定すると、テーブルの実装者は、その 1 つを処理する前に、いくつかの呼び出し \_ を収集できます。</span><span class="sxs-lookup"><span data-stu-id="93501-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="93501-117">リモート サーバーに対して潜在的に多くの呼び出しを行う代わりに。テーブル実装者は 1 つを作成し、すべての操作を一度に実行できます。</span><span class="sxs-lookup"><span data-stu-id="93501-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="93501-118">操作の結果は、必要になるまで評価されません。</span><span class="sxs-lookup"><span data-stu-id="93501-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="93501-119">たとえば、クライアントが [IMAPITable::Restrict](imapitable-restrict.md) を呼び出して TBL BATCH フラグを設定して制限を指定する場合、クライアントが \_ [IMAPITable::QueryRows](imapitable-queryrows.md) を呼び出してデータを取得するまで、制限を有効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="93501-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="93501-120">これにより、テーブル実装者は 2 つの呼び出しの作業を 1 に結合できます。</span><span class="sxs-lookup"><span data-stu-id="93501-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="93501-121">TBL BATCH フラグを利用するテーブル ユーザーは、これらの条件下でのエラー処理が複雑になる \_ 可能性があります。</span><span class="sxs-lookup"><span data-stu-id="93501-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="93501-122">遅延操作によるエラーの処理は、MAPI DEFERRED_ERRORS フラグが設定されている場合のエラーの処理と似ているため、詳細については \_ [、「DELAYING MAPI Errors」](deferring-mapi-errors.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93501-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="93501-123">**一般的に使用されるプロパティのキャッシュを保持する**</span><span class="sxs-lookup"><span data-stu-id="93501-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="93501-124">テーブルを実装するサービス プロバイダーは、一般的に使用されるオブジェクト プロパティのコピーをキャッシュすることで、ビューの作成にかかる時間を減らします。</span><span class="sxs-lookup"><span data-stu-id="93501-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="93501-125">これらのプロパティのコピーをメモリに保持すると、ビューを再作成する必要があるごとにオブジェクトから取得する必要が省ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="93501-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93501-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="93501-126">See also</span></span>

- [<span data-ttu-id="93501-127">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="93501-127">MAPI Tables</span></span>](mapi-tables.md)

