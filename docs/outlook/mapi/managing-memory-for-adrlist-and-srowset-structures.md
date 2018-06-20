---
title: ADRLIST と SRowSet 構造体のメモリを管理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ab582b869fb5a53d7ac4e97e039d9bde4a4f0430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801304"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="f56ee-103">ADRLIST と SRowSet 構造体のメモリを管理するには」</span><span class="sxs-lookup"><span data-stu-id="f56ee-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="f56ee-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f56ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f56ee-105">バッファーに割り当てるすべてのメモリを 1 つの**MAPIAllocateBuffer**呼び出しを可能な限り要件は、アドレス一覧、または**ADRLIST**、および行セット、または**SRowSet**、構造体を使用する場合に適用されません。</span><span class="sxs-lookup"><span data-stu-id="f56ee-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="f56ee-106">これら 2 つの構造体は、割り当てとメモリを解放するための標準的な規則の例外です。</span><span class="sxs-lookup"><span data-stu-id="f56ee-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="f56ee-107">構造体の複数のレベルが含まれている、個々 のメンバーを追加または削除を有効にするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="f56ee-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="f56ee-108">したがって、各プロパティは、個別の割り当てをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f56ee-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="f56ee-109">独自の呼び出しを**MAPIFreeBuffer**または**FreeProws**または**のいずれか 1 回の呼び出しで解放する必要があります**MAPIFreeBuffer**、 **ADRLIST**または**SRowSet**構造体の個々 のエントリごとに 1 つの呼び出しのほとんどの構造体を解放する場所FreePadrlist**。</span><span class="sxs-lookup"><span data-stu-id="f56ee-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="f56ee-110">詳細については、 [MAPIFreeBuffer](mapifreebuffer.md)、 [ADRLIST](adrlist.md)、および[SRowSet](srowset.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f56ee-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="f56ee-111">**FreeProws**と**FreePadrlist**は、これらのデータ構造体の解放を簡略化するため、MAPI によって提供される機能です。</span><span class="sxs-lookup"><span data-stu-id="f56ee-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="f56ee-112">詳細については、 [FreeProws](freeprows.md)および[FreePadrlist](freepadrlist.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f56ee-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="f56ee-113">**FreePadrlist** **ADRLIST**構造体のメモリと構造体のメンバーに関連付けられているすべてのメモリを解放します。**SRowSet**構造体の同じは**FreeProws**を行います。</span><span class="sxs-lookup"><span data-stu-id="f56ee-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="f56ee-114">次の図は、必要な別のメモリが割り当てられたことを示す、 **ADRLIST**データ構造体のレイアウトを示しています。</span><span class="sxs-lookup"><span data-stu-id="f56ee-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="f56ee-115">灰色のボックスを表示すると、メモリを割り当てられ、1 回の呼び出しでリリースされたことができます。</span><span class="sxs-lookup"><span data-stu-id="f56ee-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="f56ee-116">**ADRLIST メモリの割り当て**</span><span class="sxs-lookup"><span data-stu-id="f56ee-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="f56ee-117">![ADRLIST メモリの割り当て](media/amapi_52.gif "ADRLIST メモリの割り当て")</span><span class="sxs-lookup"><span data-stu-id="f56ee-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f56ee-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="f56ee-118">See also</span></span>

- [<span data-ttu-id="f56ee-119">MAPI でのメモリを管理します。</span><span class="sxs-lookup"><span data-stu-id="f56ee-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

