---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397024"
---
# <a name="olfi"></a><span data-ttu-id="c60db-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="c60db-103">OLFI</span></span>

  
  
<span data-ttu-id="c60db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c60db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c60db-105">新しいメッセージまたはオフライン モードでのフォルダーのエントリ ID を割り当てるには、個人用フォルダー ファイル (PST) のストア プロバイダーによって使用される ID 構造体は、常に長期的なキューです。</span><span class="sxs-lookup"><span data-stu-id="c60db-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c60db-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c60db-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="c60db-107">Members</span><span class="sxs-lookup"><span data-stu-id="c60db-107">Members</span></span>

 <span data-ttu-id="c60db-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="c60db-108">_ulVersion_</span></span>
  
- <span data-ttu-id="c60db-109">構造体のバージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="c60db-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="c60db-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="c60db-110">_muidReserved_</span></span>
  
- <span data-ttu-id="c60db-111">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c60db-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="c60db-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="c60db-112">_ulReserved_</span></span>
  
- <span data-ttu-id="c60db-113">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c60db-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="c60db-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="c60db-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="c60db-115">割り当てに使用可能なエントリの数です。</span><span class="sxs-lookup"><span data-stu-id="c60db-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="c60db-116">これらのエントリは、同じグローバル一意識別子 (GUID) を共有します。</span><span class="sxs-lookup"><span data-stu-id="c60db-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="c60db-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="c60db-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="c60db-118">使用可能なエントリ次の割り当ての数です。</span><span class="sxs-lookup"><span data-stu-id="c60db-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="c60db-119">これらのエントリは、同じ GUID を共有します。</span><span class="sxs-lookup"><span data-stu-id="c60db-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="c60db-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="c60db-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="c60db-121">長期的な ID の構造、 **[LTID](ltid.md)** 割り当ての現在利用可能なエントリを識別します。</span><span class="sxs-lookup"><span data-stu-id="c60db-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="c60db-122">ID の長期的な構造には、GUID と、ストア内のオブジェクトを識別するインデックスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c60db-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="c60db-123">同時に、GUID とインデックスは、オブジェクトの一意のエントリ ID を形成できます。</span><span class="sxs-lookup"><span data-stu-id="c60db-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="c60db-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="c60db-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="c60db-125">長期的な ID の構造が次の使用可能なエントリを識別します。</span><span class="sxs-lookup"><span data-stu-id="c60db-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c60db-126">備考</span><span class="sxs-lookup"><span data-stu-id="c60db-126">Remarks</span></span>

<span data-ttu-id="c60db-127">エントリ ID は、フォルダーまたはメッセージの 4 バイト MAPI エントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="c60db-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="c60db-128">詳細については、[エントリ ID](https://msdn.microsoft.com/library/ms836424)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c60db-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="c60db-129">PST ストア プロバイダーは、新しいオブジェクトのエントリ ID を割り当てます、ときに、サーバーを識別する GUID とストア内のオブジェクトを識別するインデックスが最初に必要です。</span><span class="sxs-lookup"><span data-stu-id="c60db-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="c60db-130">GUID は、すべてのエントリ Id の間では一意ではありません、でも GUID と組み合わせてインデックスは、一意のエントリを提供します。</span><span class="sxs-lookup"><span data-stu-id="c60db-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="c60db-131">この GUID とインデックスの組み合わせは、 **OLFI**構造体の一部である構造体で長期的な ID、 **LTID**、追跡されます。</span><span class="sxs-lookup"><span data-stu-id="c60db-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="c60db-132">PST ストア プロバイダーに物理的に保持しない**OLFI**の GUID インデックスごとの**LTID**構造体です。</span><span class="sxs-lookup"><span data-stu-id="c60db-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="c60db-133">*LtidAlloc* 、利用可能なの現在の最初の GUID インデックス組の 1 つの**LTID**構造が保たれます*dwAlloc* 、この同じ GUID を共有する利用可能なエントリの数をカウント2 番目の**LTID**構造、 *ltidNextAlloc* 、異なる GUID を持つ次の使用可能な GUID インデックス組の。</span><span class="sxs-lookup"><span data-stu-id="c60db-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="c60db-134">PST は、プロバイダーは Guid と渡すことは、インデックスを追跡するために**OLFI**構造体を格納します。仮想レベルは、プロバイダーは、割り当てられる準備ができている**LTID**構造体の数の予約を保持します。</span><span class="sxs-lookup"><span data-stu-id="c60db-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="c60db-135">*dwAlloc*は、使用可能の**LTID**の構造体の数を保持します。</span><span class="sxs-lookup"><span data-stu-id="c60db-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="c60db-136">エントリ Id の要求はブロックがあります。</span><span class="sxs-lookup"><span data-stu-id="c60db-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="c60db-137">ブロックの要求がある場合は、PST ストア プロバイダーがあるかどうか十分な予約に対し*dwAlloc*で要求されたサイズを比較することによってを確認します。</span><span class="sxs-lookup"><span data-stu-id="c60db-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="c60db-138">十分な予約がある場合は、割り当てのための*ltidAlloc*のインデックス、GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="c60db-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="c60db-139">*DwAlloc*を要求されたサイズが減少し、要求されたサイズを指定して*ltidAlloc*内のインデックスをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="c60db-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="c60db-140">これは、PST ストア プロバイダーは、次の要求を*ltidAlloc*のエントリ Id のもう 1 つのブロックの割り当てを準備します。</span><span class="sxs-lookup"><span data-stu-id="c60db-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="c60db-141">GUID は次の要求に同じことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c60db-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="c60db-142">要求のサイズが*dwAlloc*よりも大きい場合は、PST ストア プロバイダーがあるか次の予約の場合、 *dwNextAlloc*と*ltidNextAlloc*で指定されたを使用しようとします。</span><span class="sxs-lookup"><span data-stu-id="c60db-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="c60db-143">*DwAlloc*と*ltidAlloc*をそれぞれ、 *dwNextAlloc*と*ltidNextAlloc*をコピーし、 *dwNextAlloc*と*ltidNextAlloc*を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="c60db-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="c60db-144">PST ストア プロバイダーをラップするプロバイダーは、それが NULL であるかどうかを*ltidNextAlloc*を定期的にチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c60db-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="c60db-145">場合は、プロバイダーは新しい GUID を設定し、 *dwNextAlloc*をリセットして、複数のエントリ Id を割り当てることができる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c60db-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c60db-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="c60db-146">See also</span></span>



[<span data-ttu-id="c60db-147">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="c60db-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c60db-148">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="c60db-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c60db-149">LTID</span><span class="sxs-lookup"><span data-stu-id="c60db-149">LTID</span></span>](ltid.md)

