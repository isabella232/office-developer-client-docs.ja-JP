---
title: テーブルを使用するためのヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339649"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="90cc5-103">テーブルを使用するためのヒント</span><span class="sxs-lookup"><span data-stu-id="90cc5-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="90cc5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90cc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90cc5-105">MAPI テーブルを使用することは、リレーショナルデータベーステーブルを処理するのと似ています。</span><span class="sxs-lookup"><span data-stu-id="90cc5-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="90cc5-106">ユーザーは、ビュー内の行数と列数を制限し、その順序を指定できます。</span><span class="sxs-lookup"><span data-stu-id="90cc5-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="90cc5-107">行は、一度に1つまたは複数のグループで取得できます。</span><span class="sxs-lookup"><span data-stu-id="90cc5-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="90cc5-108">現在の位置を追跡するカーソルは、テーブルの特定の位置に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="90cc5-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="90cc5-109">テーブルを使用する場合、クライアントは、サービスプロバイダーとして、テーブルの基になるデータを所有しているかどうかに応じて、読み取り専用のインターフェイス、 \*\*\*\* [IMAPITable: iunknown](imapitableiunknown.md)を使用します。 [](itabledataiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="90cc5-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="90cc5-110">これらのインターフェイスで定義されている操作は、テーブルのすべてのユーザーが、より高度な処理を実行したり、頻繁に使用されていない操作を実行したりできる操作として分類できます。</span><span class="sxs-lookup"><span data-stu-id="90cc5-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="90cc5-111">高度な操作の一部は、実装が複雑になります。他のユーザーは複雑ではありませんが、少数の MAPI コンポーネントに関連しています。</span><span class="sxs-lookup"><span data-stu-id="90cc5-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="90cc5-112">一般的な操作は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="90cc5-112">The more common operations are:</span></span>
  
- <span data-ttu-id="90cc5-113">列の操作。単一の列に影響します。</span><span class="sxs-lookup"><span data-stu-id="90cc5-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="90cc5-114">これには、列セットに含めるプロパティと、それらを含める順序を指定することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="90cc5-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="90cc5-115">行の操作。1つの行に影響します。</span><span class="sxs-lookup"><span data-stu-id="90cc5-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="90cc5-116">これには、データの取得とメンテナンス操作が含まれます。これには、1つの行または行の追加、削除、および変更があります。</span><span class="sxs-lookup"><span data-stu-id="90cc5-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="90cc5-117">テーブル全体に影響を与えるグローバル操作。</span><span class="sxs-lookup"><span data-stu-id="90cc5-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="90cc5-118">これらには、イベント通知、検索、並べ替えが含まれます。</span><span class="sxs-lookup"><span data-stu-id="90cc5-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90cc5-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="90cc5-119">See also</span></span>



[<span data-ttu-id="90cc5-120">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="90cc5-120">MAPI Tables</span></span>](mapi-tables.md)

