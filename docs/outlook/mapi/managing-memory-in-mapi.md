---
title: MAPI でのメモリを管理します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c30aa631e70f8f4be52c2fd42dd6bfad900f379e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566160"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="5c1e6-103">MAPI でのメモリを管理します。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="5c1e6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c1e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c1e6-105">方法とタイミングを割り当てるし、メモリを解放するのには、MAPI を使用するプログラミングの重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="5c1e6-106">MAPI には、関数とマクロの両方を一貫した方法でメモリを管理するために、クライアントまたはサービス プロバイダーを使用できますが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="5c1e6-107">3 つの関数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="5c1e6-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5c1e6-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5c1e6-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="5c1e6-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="5c1e6-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5c1e6-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="5c1e6-111">クライアントとサービス ・ プロバイダーの問題、これらの関数を使用する場合の「所有者」-をリリースする方法を知っているが、-特定のメモリ ブロックを削除します。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="5c1e6-112">サービス プロバイダーのメソッドを呼び出すクライアントは、任意のサイズの戻り値を保持するのに十分な大きさのバッファーを渡す必要がありますありません。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="5c1e6-113">サービス プロバイダーは、 **MAPIAllocateBuffer**を使用しているメモリの適切な量を割り当てることが単にし、必要に応じて、 **MAPIAllocateMore**、およびクライアントが後で元の**MAPIFreeBuffer**サービスに関係なくを使用してはプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="5c1e6-114">構造体または特定のサイズの構造体の配列を割り当てるメモリのマクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="5c1e6-115">クライアントとサービス ・ プロバイダーする必要がありますこれらのマクロを使用してではなく手動でメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="5c1e6-116">などの場合は、クライアントは、名前解決の 3 つのエントリを持つ受信者リストの処理を実行する必要がある、 **SizedADRLIST**マクロ使えますの正しい数を**IAddrBook::ResolveName**に渡すための**ADRLIST**構造体を作成するには**ADRENTRY**メンバー。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="5c1e6-117">すべてのメモリ ・ マクロは、MAPIDEFS で定義されます。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="5c1e6-118">これらのマクロは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="5c1e6-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="5c1e6-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="5c1e6-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="5c1e6-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="5c1e6-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="5c1e6-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="5c1e6-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="5c1e6-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="5c1e6-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="5c1e6-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="5c1e6-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="5c1e6-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="5c1e6-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="5c1e6-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="5c1e6-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5c1e6-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="5c1e6-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="5c1e6-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="5c1e6-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="5c1e6-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="5c1e6-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="5c1e6-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="5c1e6-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="5c1e6-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="5c1e6-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="5c1e6-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="5c1e6-132">MAPI には、メモリ管理に[IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx)の COM インターフェイスの使用もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-132">MAPI also supports the use of the COM interface [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="5c1e6-133">サービス プロバイダーは、 **IMalloc**インターフェイス ポインター式によって与えられます MAPI の初期化時と、 [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md)関数を 1 つを取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="5c1e6-134">**IMalloc**メソッドを使用して MAPI の関数でメモリを管理するために主な利点は COM メソッドを使用して既存のバッファーを再割り当てすることです。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="5c1e6-135">MAPI メモリ関数は、再割り当てをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5c1e6-135">The MAPI memory functions do not support reallocation.</span></span> 
  

