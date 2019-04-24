---
title: ADRLIST および SRowSet 構造のためのメモリ管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298130"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="6d786-103">adrlist および srowset 構造体のメモリの管理 "</span><span class="sxs-lookup"><span data-stu-id="6d786-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="6d786-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d786-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d786-105">単一の**MAPIAllocateBuffer**呼び出しで、可能な場合には、アドレス一覧、 **adrlist**、行セット、または**srowset**、構造体を使用している場合には、バッファーのすべてのメモリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d786-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="6d786-106">これらの2つの構造体は、メモリを割り当てて解放するための標準的な規則の例外です。</span><span class="sxs-lookup"><span data-stu-id="6d786-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="6d786-107">複数のレベルの構造が含まれており、個々のメンバーを追加または削除できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6d786-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="6d786-108">そのため、各プロパティは個別に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d786-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="6d786-109">ほとんどの構造体は**MAPIFreeBuffer**への呼び出しによって解放されます。 **adrlist**構造体または**srowset**構造体内の個々のエントリは、 **MAPIFreeBuffer**への独自の呼び出し、または**freeprows**への1回の呼び出しで解放する必要があります。または **、freepadrlist**。</span><span class="sxs-lookup"><span data-stu-id="6d786-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="6d786-110">詳細については、「 [MAPIFreeBuffer](mapifreebuffer.md)」、「 [adrlist](adrlist.md)」、および「 [srowset](srowset.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d786-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="6d786-111">**freeprows**および**freepadrlist**は、これらのデータ構造の解放を簡略化するために MAPI によって提供される機能です。</span><span class="sxs-lookup"><span data-stu-id="6d786-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="6d786-112">詳細については、「 [freeprows](freeprows.md) 」および「 [freepadrlist](freepadrlist.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d786-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="6d786-113">**freepadrlist**は、 **adrlist**構造体のメモリと、構造体メンバーに関連付けられているすべてのメモリを解放します。**freeprows**は、 **srowset**構造に対して同じことを行います。</span><span class="sxs-lookup"><span data-stu-id="6d786-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="6d786-114">次の図は、 **adrlist**データ構造のレイアウトを示しています。これは、別のメモリ割り当てが必要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="6d786-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="6d786-115">灰色のボックスには、1回の呼び出しで割り当てたり解放したりできるメモリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d786-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="6d786-116">**ADRLIST メモリの割り当て**</span><span class="sxs-lookup"><span data-stu-id="6d786-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="6d786-117">![adrlist のメモリ割り当て](media/amapi_52.gif "adrlist のメモリ割り当て")</span><span class="sxs-lookup"><span data-stu-id="6d786-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d786-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d786-118">See also</span></span>

- [<span data-ttu-id="6d786-119">MAPI でのメモリの管理</span><span class="sxs-lookup"><span data-stu-id="6d786-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

