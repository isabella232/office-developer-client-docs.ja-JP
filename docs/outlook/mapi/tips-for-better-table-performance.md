---
title: テーブルのパフォーマンスを向上させるためのヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2b14c4fe8cbbadb2ccdd6a2f7870a07d2f96a3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804107"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="e24ab-103">テーブルのパフォーマンスを向上させるためのヒント</span><span class="sxs-lookup"><span data-stu-id="e24ab-103">Tips for better table performance</span></span>
  
<span data-ttu-id="e24ab-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e24ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e24ab-105">テーブル操作の多くは時間がかかり、進行状況を示す方法がないため、パフォーマンスを向上させるための次の方法を使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="e24ab-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="e24ab-106">**作成[IMAPITable: IUnknown](imapitableiunknown.md) 、正しい順序で呼び出す**</span><span class="sxs-lookup"><span data-stu-id="e24ab-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="e24ab-107">クライアントとサービス ・ プロバイダーは、さまざまな方法でテーブルを操作できます。</span><span class="sxs-lookup"><span data-stu-id="e24ab-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="e24ab-108">テーブルを開き、すべての既定の列セットを使用して行のデータを取得し、並べ替え順序をことができます。</span><span class="sxs-lookup"><span data-stu-id="e24ab-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="e24ab-109">代わりに、この既定のビュー、テーブルの列セットを変更する、並べ替え順序を変更する、またはテーブルの範囲を絞り込むには制限を確立することによって変更します。</span><span class="sxs-lookup"><span data-stu-id="e24ab-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="e24ab-110">すべてのデータを取得する前にこれらの操作のいずれかを実行する予定があるテーブル ユーザーは、次の順序でを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e24ab-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="e24ab-111">[IMAPITable::SetColumns](imapitable-setcolumns.md)に設定されている列を定義します。</span><span class="sxs-lookup"><span data-stu-id="e24ab-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="e24ab-112">[IMAPITable::Restrict](imapitable-restrict.md)の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="e24ab-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="e24ab-113">[IMAPITable::SortTable](imapitable-sorttable.md)での並べ替え順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="e24ab-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="e24ab-114">次の順序でこれらのタスクを実行すると、行と列を並べ替えるとき、それによってパフォーマンスが向上する数が制限されます。</span><span class="sxs-lookup"><span data-stu-id="e24ab-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="e24ab-115">**可能な場合、TBL_BATCH フラグを使用して操作を遅延させる**</span><span class="sxs-lookup"><span data-stu-id="e24ab-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="e24ab-116">テーブルを設定する\_メソッドでのバッチのフラグにより、それらのいずれかのアクションを実行する前にいくつかの呼び出しを収集するためにテーブルの作成者です。</span><span class="sxs-lookup"><span data-stu-id="e24ab-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="e24ab-117">代わりにリモート サーバーへの可能性がある多くの呼び出しを行うテーブルの作成者は作成、すべての操作を同時に実行します。</span><span class="sxs-lookup"><span data-stu-id="e24ab-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="e24ab-118">必要でない限り、操作の結果は評価されません。</span><span class="sxs-lookup"><span data-stu-id="e24ab-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="e24ab-119">クライアントが、テーブルの制限を指定する[IMAPITable::Restrict](imapitable-restrict.md)を呼び出すと、\_バッチ フラグが設定を有効に、クライアントがデータを取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出すまで、制限は必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e24ab-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="e24ab-120">これにより、2 つの呼び出しを 1 つの作業を結合するテーブルの作成者です。</span><span class="sxs-lookup"><span data-stu-id="e24ab-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="e24ab-121">テーブル、テーブルを利用するユーザー\_バッチのフラグより複雑なエラー条件を処理できることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e24ab-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="e24ab-122">エラーの処理に似ていますが、遅延操作からのエラーを処理するために MAPI\_DEFERRED_ERRORS フラグが設定されて、詳細については[保留する MAPI エラー](deferring-mapi-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e24ab-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="e24ab-123">**一般的に使用されるプロパティのキャッシュを保持します。**</span><span class="sxs-lookup"><span data-stu-id="e24ab-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="e24ab-124">テーブルを実装するサービス プロバイダーは、一般的に使用されるオブジェクトのプロパティのコピーをキャッシュすることによってビューを作成するのにかかる時間を軽減できます。</span><span class="sxs-lookup"><span data-stu-id="e24ab-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="e24ab-125">メモリ保存のたびに、オブジェクトから取得することで、ビューのこれらのプロパティのコピーを保持することは再構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e24ab-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e24ab-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="e24ab-126">See also</span></span>

- [<span data-ttu-id="e24ab-127">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="e24ab-127">MAPI Tables</span></span>](mapi-tables.md)

