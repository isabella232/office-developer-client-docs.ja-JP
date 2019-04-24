---
title: MAPI でのメモリの管理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298097"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="6fb07-103">MAPI でのメモリの管理</span><span class="sxs-lookup"><span data-stu-id="6fb07-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="6fb07-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fb07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fb07-105">メモリの割り当てと解放の方法とタイミングを知ることは、MAPI を使用したプログラミングの重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="6fb07-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="6fb07-106">MAPI には、クライアントまたはサービスプロバイダーが一貫した方法でメモリを管理するために使用できる関数とマクロの両方が用意されています。</span><span class="sxs-lookup"><span data-stu-id="6fb07-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="6fb07-107">3つの関数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6fb07-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="6fb07-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="6fb07-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="6fb07-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="6fb07-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="6fb07-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6fb07-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="6fb07-111">クライアントおよびサービスプロバイダーがこれらの機能を使用する場合、誰がどのようなメモリブロックを解放するかを知ることができます。</span><span class="sxs-lookup"><span data-stu-id="6fb07-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="6fb07-112">サービスプロバイダメソッドを呼び出すクライアントは、任意のサイズの戻り値を保持するために十分に大きいバッファーを通過する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6fb07-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="6fb07-113">サービスプロバイダーは単に、 **MAPIAllocateBuffer**を使用して適切な量のメモリを割り当てることができ、必要に応じて**MAPIAllocateMore**、クライアントは後で**MAPIFreeBuffer**を使用して、サービスに依存することなく、そのメモリを解放できます。供給.</span><span class="sxs-lookup"><span data-stu-id="6fb07-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="6fb07-114">メモリマクロは、構造体または特定のサイズの構造の配列を割り当てるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6fb07-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="6fb07-115">クライアントおよびサービスプロバイダーは、メモリを手動で割り当てる代わりに、これらのマクロを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fb07-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="6fb07-116">たとえば、クライアントが3つのエントリを持つ受信者リストで名前解決処理を実行する必要がある場合、 **sizedadrlist**マクロを使用して、 **IAddrBook:: ResolveName**に渡される**adrlist**構造を作成し、正しい数の**adrentry**のメンバー。</span><span class="sxs-lookup"><span data-stu-id="6fb07-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="6fb07-117">mapidefs.h では、すべてのメモリマクロが定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="6fb07-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="6fb07-118">これらのマクロは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6fb07-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="6fb07-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="6fb07-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="6fb07-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="6fb07-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="6fb07-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="6fb07-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="6fb07-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="6fb07-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="6fb07-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="6fb07-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="6fb07-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6fb07-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="6fb07-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="6fb07-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="6fb07-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6fb07-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="6fb07-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="6fb07-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="6fb07-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="6fb07-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="6fb07-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="6fb07-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="6fb07-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="6fb07-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="6fb07-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="6fb07-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="6fb07-132">MAPI では、メモリ管理用の COM インターフェイス[imalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx)の使用もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6fb07-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="6fb07-133">サービスプロバイダーには、初期化時に MAPI によって**imalloc**インターフェイスポインターが与えられ、 [mapigetdefaultmalloc](mapigetdefaultmalloc.md)関数を使用して取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="6fb07-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="6fb07-134">MAPI 関数でメモリを管理するために**imalloc**メソッドを使用する主な利点は、COM メソッドを使用して既存のバッファーを再割り当てできることです。</span><span class="sxs-lookup"><span data-stu-id="6fb07-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="6fb07-135">MAPI メモリ関数は再割り当てをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6fb07-135">The MAPI memory functions do not support reallocation.</span></span> 
  

