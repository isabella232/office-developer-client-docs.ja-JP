---
title: ヒント操作の詳細
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439738"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="26706-103">ヒント操作の詳細</span><span class="sxs-lookup"><span data-stu-id="26706-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="26706-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26706-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26706-105">MAPI テーブルの操作は、リレーショナル データベース テーブルの操作と少し似たものになります。</span><span class="sxs-lookup"><span data-stu-id="26706-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="26706-106">ユーザーは、ビュー内の行と列の数を制限し、その順序を指定できます。</span><span class="sxs-lookup"><span data-stu-id="26706-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="26706-107">行は、一度に 1 つ、またはグループで取得できます。</span><span class="sxs-lookup"><span data-stu-id="26706-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="26706-108">現在の位置を追跡するカーソルは、テーブル内の特定の場所に移動できます。</span><span class="sxs-lookup"><span data-stu-id="26706-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="26706-109">テーブルを使用するには、クライアントは読み取り専用インターフェイス [IMAPITable : IUnknown](imapitableiunknown.md)を使用しますが、サービス プロバイダーは、テーブルが基づくデータを所有するかどうかに応じて **、IMAPITable** または [ITableData : IUnknown](itabledataiunknown.md)を使用できます。</span><span class="sxs-lookup"><span data-stu-id="26706-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="26706-110">これらのインターフェイスで定義された操作は、テーブルのすべてのユーザーが実行または呼び出す操作、および高度な操作が行われるため、広く使用されていない操作として分類できます。</span><span class="sxs-lookup"><span data-stu-id="26706-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="26706-111">高度な操作の中には、実装が複雑な操作があります。他のコンポーネントは複雑ではなく、MAPI コンポーネントの少数派に関心があります。</span><span class="sxs-lookup"><span data-stu-id="26706-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="26706-112">より一般的な操作は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="26706-112">The more common operations are:</span></span>
  
- <span data-ttu-id="26706-113">1 つの列に影響する列操作。</span><span class="sxs-lookup"><span data-stu-id="26706-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="26706-114">これには、列セットに含めるプロパティと、列セットを含める順序の指定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="26706-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="26706-115">1 つの行に影響する行操作。</span><span class="sxs-lookup"><span data-stu-id="26706-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="26706-116">これには、データ取得とメンテナンス操作 (1 行または 1 行の追加、削除、変更) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="26706-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="26706-117">テーブル全体に影響を与えるグローバル操作。</span><span class="sxs-lookup"><span data-stu-id="26706-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="26706-118">これには、イベント通知、検索、並べ替えが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26706-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26706-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="26706-119">See also</span></span>



[<span data-ttu-id="26706-120">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="26706-120">MAPI Tables</span></span>](mapi-tables.md)

