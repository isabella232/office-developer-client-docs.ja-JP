---
title: MAPI でのメモリの管理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298097"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="b8e9a-103">MAPI でのメモリの管理</span><span class="sxs-lookup"><span data-stu-id="b8e9a-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="b8e9a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8e9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8e9a-105">メモリを割り当て、解放する方法と時間を知ることは、MAPI を使用したプログラミングの重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="b8e9a-106">MAPI には、クライアントまたはサービス プロバイダーが一貫した方法でメモリを管理するために使用できる関数とマクロの両方が提供されています。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="b8e9a-107">3 つの関数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="b8e9a-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="b8e9a-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="b8e9a-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="b8e9a-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="b8e9a-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b8e9a-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="b8e9a-111">クライアントとサービス プロバイダーがこれらの関数を使用すると、特定のメモリ ブロックを解放する方法を知っているユーザー (つまり、所有するユーザー) の問題が解消されます。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="b8e9a-112">サービス プロバイダー メソッドを呼び出すクライアントは、任意のサイズの戻り値を保持するのに十分な大きさのバッファーを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="b8e9a-113">サービス プロバイダーは **、MAPIAllocateBuffer** を使用して適切な量のメモリを割り当て、必要に応じて **MAPIAllocateMore** を割り当て、クライアントは、サービス プロバイダーとは別に **、MAPIFreeBuffer** を使用して後で解放できます。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="b8e9a-114">メモリ マクロは、特定のサイズの構造体または構造体の配列を割り当てるのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="b8e9a-115">クライアントとサービス プロバイダーは、メモリを手動で割り当てるのではなく、これらのマクロを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="b8e9a-116">たとえば、クライアントが 3 つのエントリを含む受信者リストで名前解決処理を実行する必要がある場合 **、SizedADRLIST** マクロを使用して、正しい数の **ADRENTRY** メンバーを持つ **IAddrBook::ResolveName** に渡す **ADRLIST** 構造を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="b8e9a-117">すべてのメモリ マクロは MAPIDEFS で定義されています。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="b8e9a-118">これらのマクロは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="b8e9a-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="b8e9a-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="b8e9a-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="b8e9a-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="b8e9a-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="b8e9a-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="b8e9a-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="b8e9a-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="b8e9a-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="b8e9a-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="b8e9a-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b8e9a-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="b8e9a-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="b8e9a-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="b8e9a-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b8e9a-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="b8e9a-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="b8e9a-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="b8e9a-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="b8e9a-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="b8e9a-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="b8e9a-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="b8e9a-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b8e9a-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="b8e9a-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="b8e9a-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="b8e9a-132">MAPI は、メモリ管理のための COM インターフェイス [IMalloc の](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) 使用もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="b8e9a-133">サービス プロバイダーには、初期化時に MAPI によって **IMalloc** インターフェイス ポインターが与え [、MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) 関数を介して取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="b8e9a-134">**IMalloc** メソッドを使用して MAPI 関数を使用してメモリを管理する主な利点は、COM メソッドを使用すると、既存のバッファーを再割り当てできるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="b8e9a-135">MAPI メモリ関数は、割り当て解除をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="b8e9a-135">The MAPI memory functions do not support reallocation.</span></span> 
  

