---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279754"
---
# <a name="olfi"></a><span data-ttu-id="b1fbf-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="b1fbf-103">OLFI</span></span>

  
  
<span data-ttu-id="b1fbf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1fbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1fbf-105">個人用フォルダー ファイル (PST) ストア プロバイダーがオフライン モードで新しいメッセージまたはフォルダーのエントリ ID を割り当てるのに使用する長期 ID 構造のキュー。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b1fbf-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b1fbf-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a><span data-ttu-id="b1fbf-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="b1fbf-107">Members</span></span>

 <span data-ttu-id="b1fbf-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="b1fbf-108">_ulVersion_</span></span>
  
- <span data-ttu-id="b1fbf-109">構造のバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="b1fbf-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="b1fbf-110">_muidReserved_</span></span>
  
- <span data-ttu-id="b1fbf-111">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="b1fbf-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="b1fbf-112">_ulReserved_</span></span>
  
- <span data-ttu-id="b1fbf-113">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="b1fbf-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="b1fbf-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="b1fbf-115">割り当てに使用できるエントリの数。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="b1fbf-116">これらのエントリは、同じグローバル一意識別子 (GUID) を共有します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="b1fbf-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="b1fbf-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="b1fbf-118">次に割り当てに使用できるエントリの数。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="b1fbf-119">これらのエントリは同じ GUID を共有します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="b1fbf-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="b1fbf-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="b1fbf-121">長期 ID 構造 **[LTID](ltid.md)** は、現在割り当て可能なエントリを識別します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="b1fbf-122">長期的な ID 構造には、GUID と、ストア内のオブジェクトを識別するインデックスが含まれる。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="b1fbf-123">GUID とインデックスを組み合わせて、オブジェクトの一意のエントリ ID を形成できます。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="b1fbf-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="b1fbf-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="b1fbf-125">次に使用可能なエントリを識別する長期 ID 構造。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1fbf-126">注釈</span><span class="sxs-lookup"><span data-stu-id="b1fbf-126">Remarks</span></span>

<span data-ttu-id="b1fbf-127">エントリ ID は、フォルダーまたはメッセージの 4 バイトの MAPI エントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="b1fbf-128">詳細については [、「ENTRYID」を参照してください](https://msdn.microsoft.com/library/ms836424)。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="b1fbf-129">PST ストア プロバイダーがエントリ ID を新しいオブジェクトに割り当てる場合、最初にサーバーを識別する GUID と、ストア内のオブジェクトを識別するインデックスが必要です。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="b1fbf-130">GUID がすべてのエントリ ID で一意ではない場合でも、GUID とインデックスの組み合わせによって一意のエントリが提供されます。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="b1fbf-131">この GUID とインデックスのペアは **、OLFI** 構造の一部である長期 ID 構造 LTID **によって追跡** されます。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="b1fbf-132">PST ストア プロバイダーは、GUID インデックスのペアごとに **OLFI** **に LTID** 構造を物理的に保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="b1fbf-133">現在使用可能な **最初の GUID-index** ペアに対して 1 つの LTID 構造  *ltidAlloc*  を保持します。この同じ GUID を共有する使用可能なエントリの数である  *dwAlloc。*  2 番目 **の LTID** 構造体  *ltidNextAlloc*  は、別の GUID を持つ次に使用可能な GUID-index ペア用です。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="b1fbf-134">PST ストア プロバイダーは **、OLFI** 構造を使用して、渡した GUID とインデックスを追跡します。仮想レベルでは、プロバイダーは、割り当て可能な多数の **LTID** 構造の予約を保持します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="b1fbf-135">*dwAlloc は*  、使用可能な LTID 構造の数 **を維持** します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="b1fbf-136">エントリの ID の要求はブロック内に含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="b1fbf-137">ブロックの要求がある場合、PST ストア プロバイダーは、要求されたサイズと  *dwAlloc*  を比較して、準備金が十分にあるか確認します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="b1fbf-138">十分な予約がある場合は、割り当て用に  *ltidAlloc*  の GUID とインデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="b1fbf-139">次に、  *要求されたサイズで dwAlloc*  を小さめ、要求されたサイズで  *ltidAlloc*  のインデックスをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="b1fbf-140">これにより、PST ストア プロバイダーは、エントリ ID の別のブロックに対する次の要求に  *ltidAlloc*  を割り当てる準備をします。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="b1fbf-141">次の要求に対して GUID は同じままです。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="b1fbf-142">要求のサイズが  *dwAlloc*  より大きい場合、PST ストア プロバイダーは  *、dwNextAlloc*  および  *ltidNextAlloc*  で指定された次の予約内にある要求を使用します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="b1fbf-143">*dwNextAlloc* と *ltidNextAlloc* をそれぞれ *dwAlloc* と *ltidAlloc* にコピーし *、dwNextAlloc* と *ltidNextAlloc* を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="b1fbf-144">PST ストア プロバイダーをラップするプロバイダーは、定期的に  *ltidNextAlloc*  をチェックして NULL を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="b1fbf-145">その場合、プロバイダーは新しい GUID を設定し、より多くのエントリ ID を割り当て可能に  *dwNextAlloc*  をリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1fbf-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1fbf-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1fbf-146">See also</span></span>



[<span data-ttu-id="b1fbf-147">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b1fbf-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b1fbf-148">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="b1fbf-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b1fbf-149">LTID</span><span class="sxs-lookup"><span data-stu-id="b1fbf-149">LTID</span></span>](ltid.md)

