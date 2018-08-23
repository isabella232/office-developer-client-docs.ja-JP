---
title: テーブルの操作のヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 451bab57d4e2e8669a25d119f9ce28a8f78e628f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804099"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="c0bc9-103">テーブルの操作のヒント</span><span class="sxs-lookup"><span data-stu-id="c0bc9-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="c0bc9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0bc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0bc9-105">MAPI を使用するテーブルは、リレーショナル データベースのテーブルに like 作業を少しです。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="c0bc9-106">ユーザーは、ビューの行と列の数を制限し、それらの順序を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="c0bc9-107">行には、同時にまたはグループで、取得した 1 つをすることができます。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="c0bc9-108">カーソルの現在位置を追跡するテーブル内の特定の場所に移動できます。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="c0bc9-109">テーブルを使用するクライアント インターフェイスを使用して、読み取り専用、 [IMAPITable: IUnknown](imapitableiunknown.md)テーブルの基になっているデータを所有するかどうかによって、サービス プロバイダーが**IMAPITable**をいずれかを使用できますが、または[ITableData: IUnknown](itabledataiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="c0bc9-110">テーブルのすべてのユーザーか、または呼び出すことができる操作と広く使用されていないためより高度な操作としては、これらのインタ フェースで定義されている操作を分類できます。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="c0bc9-111">いくつかの高度な操作は、単純に実装します。他のユーザーは複雑、ですが、ごく一部の MAPI コンポーネントに関係の。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="c0bc9-112">一般的な操作は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-112">The more common operations are:</span></span>
  
- <span data-ttu-id="c0bc9-113">列の操作、1 つの列に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="c0bc9-114">列セットと、それらを含めるように順序に含まれるプロパティを指定することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="c0bc9-115">行操作には、単一行に影響します。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="c0bc9-116">データの取得と保守作業が含まれます: 追加、削除、および 1 つの行または行を変更します。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="c0bc9-117">グローバル操作、テーブル全体に影響します。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="c0bc9-118">イベント通知、検索および並べ替えが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c0bc9-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0bc9-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0bc9-119">See also</span></span>



[<span data-ttu-id="c0bc9-120">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="c0bc9-120">MAPI Tables</span></span>](mapi-tables.md)

