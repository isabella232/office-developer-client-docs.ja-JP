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
# <a name="olfi"></a><span data-ttu-id="bcec3-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="bcec3-103">OLFI</span></span>

  
  
<span data-ttu-id="bcec3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcec3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcec3-105">個人用フォルダーファイル (PST) ストアプロバイダーが、新しいメッセージまたはフォルダーのエントリ ID をオフラインモードで割り当てるために使用する、長期 ID 構造のキュー。</span><span class="sxs-lookup"><span data-stu-id="bcec3-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bcec3-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="bcec3-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="bcec3-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="bcec3-107">Members</span></span>

 <span data-ttu-id="bcec3-108">_ulversion_</span><span class="sxs-lookup"><span data-stu-id="bcec3-108">_ulVersion_</span></span>
  
- <span data-ttu-id="bcec3-109">構造のバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="bcec3-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="bcec3-110">_muidreserved_</span><span class="sxs-lookup"><span data-stu-id="bcec3-110">_muidReserved_</span></span>
  
- <span data-ttu-id="bcec3-111">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bcec3-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="bcec3-112">_ulreserved_</span><span class="sxs-lookup"><span data-stu-id="bcec3-112">_ulReserved_</span></span>
  
- <span data-ttu-id="bcec3-113">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bcec3-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="bcec3-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="bcec3-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="bcec3-115">割り当てに使用できるエントリの数。</span><span class="sxs-lookup"><span data-stu-id="bcec3-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="bcec3-116">これらのエントリは、同じグローバル一意識別子 (GUID) を共有します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="bcec3-117">_dwnextalloc_</span><span class="sxs-lookup"><span data-stu-id="bcec3-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="bcec3-118">割り当ての次に使用可能なエントリの数。</span><span class="sxs-lookup"><span data-stu-id="bcec3-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="bcec3-119">これらのエントリは同じ GUID を共有します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="bcec3-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="bcec3-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="bcec3-121">現在割り当てられているエントリを識別する、長期的な ID 構造である**[ltid](ltid.md)**。</span><span class="sxs-lookup"><span data-stu-id="bcec3-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="bcec3-122">長期 ID 構造には、GUID と、ストア内のオブジェクトを識別するインデックスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bcec3-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="bcec3-123">また、GUID とインデックスは、オブジェクトの一意のエントリ ID を形成できます。</span><span class="sxs-lookup"><span data-stu-id="bcec3-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="bcec3-124">_ltidnextalloc_</span><span class="sxs-lookup"><span data-stu-id="bcec3-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="bcec3-125">次の利用可能なエントリを識別する長期 ID 構造。</span><span class="sxs-lookup"><span data-stu-id="bcec3-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcec3-126">解説</span><span class="sxs-lookup"><span data-stu-id="bcec3-126">Remarks</span></span>

<span data-ttu-id="bcec3-127">エントリ ID は、フォルダーまたはメッセージの4バイトの MAPI エントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="bcec3-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="bcec3-128">詳細については、「 [ENTRYID](https://msdn.microsoft.com/library/ms836424)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcec3-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="bcec3-129">PST ストアプロバイダーは、新しいオブジェクトにエントリ ID を割り当てるときに、最初にサーバーを識別する GUID と、ストア内のオブジェクトを識別するインデックスを必要とします。</span><span class="sxs-lookup"><span data-stu-id="bcec3-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="bcec3-130">guid はすべてのエントリ id で一意ではありませんが、guid とインデックスの組み合わせによって一意のエントリが提供されます。</span><span class="sxs-lookup"><span data-stu-id="bcec3-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="bcec3-131">この GUID とインデックスのペアは、 **olfi**構造の一部である、長い用語の ID 構造 ( **ltid**) によって追跡されます。</span><span class="sxs-lookup"><span data-stu-id="bcec3-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="bcec3-132">PST ストアプロバイダーでは、GUID とインデックスのペアごとに**olfi**の**ltid**構造が物理的に保持されません。</span><span class="sxs-lookup"><span data-stu-id="bcec3-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="bcec3-133">現在使用可能な最初の GUID とインデックスのペアに対して、1つの**ltid**構造*ltidAlloc*を保持します。この同じ GUID を共有する使用可能なエントリの数 ( *dwAlloc* )。もう1つ\*\*\*\* は、別の guid を持つ、次の使用可能な guid とインデックスのペアの*ltidnextalloc*です。</span><span class="sxs-lookup"><span data-stu-id="bcec3-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="bcec3-134">PST ストアプロバイダーは、 **olfi**構造を使用して、それが渡された guid とインデックスを追跡します。仮想レベルでは、プロバイダーは、割り当ての準備が整っている多数の**ltid**構造の予約を保持します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="bcec3-135">*dwAlloc*は、使用可能な**ltid**構造体のカウントを保持します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="bcec3-136">エントリ id の要求はブロックに入っています。</span><span class="sxs-lookup"><span data-stu-id="bcec3-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="bcec3-137">ブロックに対する要求がある場合、PST ストアプロバイダーは、要求されたサイズと*dwAlloc*を比較することによって、十分な予約があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="bcec3-138">十分な予約がある場合は、 *ltidAlloc*の GUID とインデックスを割り当て用に返します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="bcec3-139">その後、要求されたサイズで*dwAlloc*を減らし、要求されたサイズで*ltidAlloc*のインデックスを増分します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="bcec3-140">これにより、エントリ id の別のブロックに対する次の要求で、 *ltidAlloc*を割り当てるために PST ストアプロバイダーが準備されます。</span><span class="sxs-lookup"><span data-stu-id="bcec3-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="bcec3-141">GUID は次の要求に対して同じままであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bcec3-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="bcec3-142">要求のサイズが*dwAlloc*より大きい場合、PST ストアプロバイダーは、 *dwnextalloc*および*ltidnextalloc*で指定されている、次のものを予約で使用しようとします。</span><span class="sxs-lookup"><span data-stu-id="bcec3-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="bcec3-143">*dwnextalloc*と*ltidnalloc*をそれぞれ*dwAlloc*および*ltidAlloc*にコピーし、 *dwnextalloc*と*ltidnextalloc*を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="bcec3-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="bcec3-144">PST ストアプロバイダーをラップするプロバイダーは、 *ltidnextalloc*を定期的にチェックして、それが NULL であるかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcec3-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="bcec3-145">その場合、プロバイダーはそれを新しい GUID で設定し、さらにエントリ id を割り当てることができるように、 *dwnextalloc*をリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcec3-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bcec3-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="bcec3-146">See also</span></span>



[<span data-ttu-id="bcec3-147">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="bcec3-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bcec3-148">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="bcec3-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bcec3-149">LTID</span><span class="sxs-lookup"><span data-stu-id="bcec3-149">LTID</span></span>](ltid.md)

