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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407866"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="29d2b-103">ADRLIST および SRowSet 構造体のメモリを管理する"</span><span class="sxs-lookup"><span data-stu-id="29d2b-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="29d2b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29d2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29d2b-105">1 つの **MAPIAllocateBuffer** 呼び出しで可能な限りバッファーのすべてのメモリを割り当てる要件は、アドレス一覧または **ADRLIST**、および行セット、または **SRowSet** 構造体を使用する場合は適用されません。</span><span class="sxs-lookup"><span data-stu-id="29d2b-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="29d2b-106">これら 2 つの構造は、メモリの割り当てと解放に関する標準ルールの例外です。</span><span class="sxs-lookup"><span data-stu-id="29d2b-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="29d2b-107">これらは複数のレベルの構造を含み、個々のメンバーを追加または削除するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="29d2b-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="29d2b-108">したがって、各プロパティは個別の割り当てである必要があります。</span><span class="sxs-lookup"><span data-stu-id="29d2b-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="29d2b-109">ほとんどの構造体が **MAPIFreeBuffer** への 1 回の呼び出しで解放される場合は **、ADRLIST** 構造体または **SRowSet** 構造体の各個々のエントリを **、MAPIFreeBuffer** への独自の呼び出しまたは **FreeProws** または **FreePadrlist** への 1 回の呼び出しで解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29d2b-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="29d2b-110">詳細については [、「MAPIFreeBuffer](mapifreebuffer.md) [、ADRLIST、](adrlist.md)および [SRowSet」を参照してください](srowset.md)。</span><span class="sxs-lookup"><span data-stu-id="29d2b-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="29d2b-111">**FreeProws と** **FreePadrlist は** 、これらのデータ構造の解放を簡略化するために MAPI によって提供される関数です。</span><span class="sxs-lookup"><span data-stu-id="29d2b-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="29d2b-112">詳細については [、「FreeProws and](freeprows.md) [FreePadrlist」を参照してください](freepadrlist.md)。</span><span class="sxs-lookup"><span data-stu-id="29d2b-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="29d2b-113">**FreePadrlist は\*\*\*\*、ADRLIST** 構造体のメモリと、その構造体メンバーに関連付けられているすべてのメモリを解放します。**FreeProws は** **SRowSet 構造体でも同じことを** 行います。</span><span class="sxs-lookup"><span data-stu-id="29d2b-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="29d2b-114">次の図は **、ADRLIST** データ構造のレイアウトを示しています。必要な個別のメモリ割り当てを示します。</span><span class="sxs-lookup"><span data-stu-id="29d2b-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="29d2b-115">灰色のボックスには、1 回の呼び出しで割り当ておよび解放できるメモリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="29d2b-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="29d2b-116">**ADRLIST メモリの割り当て**</span><span class="sxs-lookup"><span data-stu-id="29d2b-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="29d2b-117">![ADRLIST メモリ割り当て](media/amapi_52.gif "ADRLIST メモリ割り当て")</span><span class="sxs-lookup"><span data-stu-id="29d2b-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29d2b-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="29d2b-118">See also</span></span>

- [<span data-ttu-id="29d2b-119">MAPI でのメモリの管理</span><span class="sxs-lookup"><span data-stu-id="29d2b-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

