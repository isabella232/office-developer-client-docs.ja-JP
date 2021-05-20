---
title: テーブルを使用したプロパティの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439913"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="85acb-103">テーブルを使用したプロパティの使用</span><span class="sxs-lookup"><span data-stu-id="85acb-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="85acb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85acb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85acb-105">多くのプロパティは、それらをサポートするオブジェクトとテーブルの列の両方から使用できます。</span><span class="sxs-lookup"><span data-stu-id="85acb-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="85acb-106">可能な限り、これらのプロパティをテーブルから取得します。</span><span class="sxs-lookup"><span data-stu-id="85acb-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="85acb-107">[IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出して、クライアントで必要なすべてのプロパティを含め[、IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出して、テーブルのすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="85acb-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="85acb-108">これらの 2 つの呼び出しは、通常、ユーザーに表示するのに十分な情報を取得するのに十分であり、必要な内部処理を行う場合は多くの場合 **、OpenEntry** を呼び出してオブジェクトを不要に開くのに十分です。</span><span class="sxs-lookup"><span data-stu-id="85acb-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="85acb-109">次の 2 つの例外があります。</span><span class="sxs-lookup"><span data-stu-id="85acb-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="85acb-110">プロパティが 255 バイトを超える場合。</span><span class="sxs-lookup"><span data-stu-id="85acb-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="85acb-111">\*\* IMAPITable \*\* インターフェイスは、プロパティ値全体を返すのではなく、255 バイトで切り捨てることはできません。</span><span class="sxs-lookup"><span data-stu-id="85acb-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="85acb-112">しかし、このトレードオフについて考えてみろ。</span><span class="sxs-lookup"><span data-stu-id="85acb-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="85acb-113">このデータをユーザーに表示する場合は、コメントなどのテキスト フィールドで 255 バイトで十分です。</span><span class="sxs-lookup"><span data-stu-id="85acb-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="85acb-114">テーブル内の 1 行から特定のプロパティが必要な場合。</span><span class="sxs-lookup"><span data-stu-id="85acb-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="85acb-115">この場合、使用しないプロパティを持つテーブルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85acb-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="85acb-116">ほとんどの場合、すべての行に同じプロパティが必要になります。</span><span class="sxs-lookup"><span data-stu-id="85acb-116">Most of the time you will need the same properties for all rows.</span></span>
    

