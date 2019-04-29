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
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="02228-103">テーブル パフォーマンス向上のためのヒント</span><span class="sxs-lookup"><span data-stu-id="02228-103">Tips for better table performance</span></span>
  
<span data-ttu-id="02228-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02228-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02228-105">テーブル操作の多くは時間がかかることがあり、進行状況を示す方法がないため、次の方法を使用してパフォーマンスを向上することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="02228-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="02228-106">**[IMAPITable: IUnknown](imapitableiunknown.md)呼び出しを正しい順序で行う**</span><span class="sxs-lookup"><span data-stu-id="02228-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="02228-107">クライアントとサービスプロバイダーは、さまざまな方法でテーブルを操作できます。</span><span class="sxs-lookup"><span data-stu-id="02228-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="02228-108">既定の列セットと並べ替え順序を使用して、テーブルを開き、すべての行のデータを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="02228-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="02228-109">または、列セットを変更したり、並べ替え順序を変更したり、テーブルの範囲を絞るために制限を設定したりすることによって、テーブルの既定のビューを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="02228-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="02228-110">テーブルデータを取得する前に、これらの操作を1つ以上実行する予定のユーザーは、次の順序で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02228-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="02228-111">[IMAPITable:: SetColumns](imapitable-setcolumns.md)を使用して、列セットを定義します。</span><span class="sxs-lookup"><span data-stu-id="02228-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="02228-112">[IMAPITable:: Restrict](imapitable-restrict.md)を使用して制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="02228-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="02228-113">[IMAPITable:: sorttable](imapitable-sorttable.md)を使用して、並べ替え順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="02228-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="02228-114">これらのタスクをこの順序で実行すると、並べ替えられる行と列の数が制限されるため、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="02228-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="02228-115">**可能であれば、TBL_BATCH フラグを使用して操作を遅延させる**</span><span class="sxs-lookup"><span data-stu-id="02228-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="02228-116">メソッドで\_一括バッチフラグを設定すると、テーブルの実装者は、そのうちの1つに処理する前に、複数の呼び出しを収集できます。</span><span class="sxs-lookup"><span data-stu-id="02228-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="02228-117">リモートサーバーに対して多くの呼び出しを行う代わりに、テーブルの実装者は、すべての操作を一度に実行することができます。</span><span class="sxs-lookup"><span data-stu-id="02228-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="02228-118">操作の結果は、必要になるまで評価されません。</span><span class="sxs-lookup"><span data-stu-id="02228-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="02228-119">たとえば、クライアントが[imapitable:: Restrict](imapitable-restrict.md)を呼び出して、\_一括バッチフラグが設定された制限を指定する場合、クライアントが[imapitable:: QueryRows](imapitable-queryrows.md)を呼び出してデータを取得するまで、制限を有効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="02228-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="02228-120">これにより、テーブルの実装側は2つの呼び出しの作業を1つにまとめることができます。</span><span class="sxs-lookup"><span data-stu-id="02228-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="02228-121">表ユーザーのテーブルフラグを利用する\_ユーザーは、このような条件下でのエラー処理がより複雑になることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="02228-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="02228-122">遅延操作でエラーを処理することは、mapi\_の DEFERRED_ERRORS フラグが設定されている場合にエラーを処理するのと似ています。詳細については、「 [mapi エラーの遅延](deferring-mapi-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02228-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="02228-123">**よく使用されるプロパティのキャッシュを保持する**</span><span class="sxs-lookup"><span data-stu-id="02228-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="02228-124">テーブルを実装するサービスプロバイダーは、よく使用されるオブジェクトプロパティのコピーをキャッシュすることによって、ビューを作成するのにかかる時間を短縮できます。</span><span class="sxs-lookup"><span data-stu-id="02228-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="02228-125">これらのプロパティのコピーをメモリに保持すると、ビューを再構築するたびにオブジェクトからそれらのプロパティを取得する手間が省けます。</span><span class="sxs-lookup"><span data-stu-id="02228-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02228-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="02228-126">See also</span></span>

- [<span data-ttu-id="02228-127">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="02228-127">MAPI Tables</span></span>](mapi-tables.md)

