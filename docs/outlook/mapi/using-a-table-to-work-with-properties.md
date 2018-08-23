---
title: テーブルを使用したプロパティの操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804189"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="0c0ac-103">テーブルを使用したプロパティの操作</span><span class="sxs-lookup"><span data-stu-id="0c0ac-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="0c0ac-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c0ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c0ac-105">多くのプロパティでは、オブジェクトがサポートするからとテーブルの列の両方が利用できます。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="0c0ac-106">可能な限り、これらのプロパティをテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="0c0ac-107">すべてのクライアントが必要なプロパティを含めるには、 [IMAPITable::SetColumns](imapitable-setcolumns.md)とすべてのテーブルの行を取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="0c0ac-108">これら 2 つの呼び出しでは、通常、ユーザーに表示するには、十分な情報を取得するため、不要なオブジェクトを開くことに**OpenEntry**呼び出しを行う、必要な内部処理のための十分な頻繁にします。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="0c0ac-109">2 つだけ例外があります。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="0c0ac-110">プロパティが 255 バイトを超える場合。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="0c0ac-111">* * IMAPITable * * インターフェイスは、代わりにそれを 255 バイトに切り捨て、全体のプロパティの値を返さない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="0c0ac-112">このトレードオフをも考えてください。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="0c0ac-113">ユーザーに、このデータを表示している場合は、255 バイトは、コメントなどのテキスト フィールドには十分で可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="0c0ac-114">場合は、テーブル内の 1 つの行から特定のプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="0c0ac-115">ここで使用することはありませんプロパティを持つテーブルを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="0c0ac-116">時間のほとんどすべての行の同じプロパティを必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c0ac-116">Most of the time you will need the same properties for all rows.</span></span>
    

