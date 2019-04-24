---
title: コンポーネント オブジェクト モデルと MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334469"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="681d7-103">コンポーネント オブジェクト モデルと MAPI</span><span class="sxs-lookup"><span data-stu-id="681d7-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="681d7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="681d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="681d7-105">Windows SDK ドキュメントには、コンポーネントオブジェクトモデル (COM) に準拠するオブジェクトを実装するための規則についての包括的な説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="681d7-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="681d7-106">これらのルールは、次の操作を実行する方法に対応しています。</span><span class="sxs-lookup"><span data-stu-id="681d7-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="681d7-107">インターフェイスとオブジェクトを設計します。</span><span class="sxs-lookup"><span data-stu-id="681d7-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="681d7-108">[IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="681d7-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="681d7-109">メモリを管理します。</span><span class="sxs-lookup"><span data-stu-id="681d7-109">Manage memory.</span></span>
    
- <span data-ttu-id="681d7-110">参照カウントを処理します。</span><span class="sxs-lookup"><span data-stu-id="681d7-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="681d7-111">アパートメントスレッドオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="681d7-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="681d7-112">すべての mapi オブジェクトは、 [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)から継承するインターフェイスを実装するため、com ベースであると見なされますが、一部の状況では、標準的な com ルールによって異なります。</span><span class="sxs-lookup"><span data-stu-id="681d7-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="681d7-113">この偏差により、開発者は実装をより柔軟にすることができます。</span><span class="sxs-lookup"><span data-stu-id="681d7-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="681d7-114">たとえば、すべての COM インターフェイスと同様に、MAPI インターフェイスは、実装側と呼び出し元との間の契約を記述します。</span><span class="sxs-lookup"><span data-stu-id="681d7-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="681d7-115">インターフェイスを作成して発行すると、その定義は変更できなくなります。</span><span class="sxs-lookup"><span data-stu-id="681d7-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="681d7-116">MAPI はこの説明から逸脱しませんが、説明は少し relaxes ます。</span><span class="sxs-lookup"><span data-stu-id="681d7-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="681d7-117">実装者は、特定のメソッドを実装しないことを選択でき、次のいずれかのエラー値を呼び出し元に返します。</span><span class="sxs-lookup"><span data-stu-id="681d7-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="681d7-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="681d7-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="681d7-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="681d7-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="681d7-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="681d7-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="681d7-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="681d7-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="681d7-122">次の表では、標準 COM ルールのその他の相違点について説明します。</span><span class="sxs-lookup"><span data-stu-id="681d7-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="681d7-123">**COM プログラミングルール**</span><span class="sxs-lookup"><span data-stu-id="681d7-123">**COM programming rule**</span></span>|<span data-ttu-id="681d7-124">**MAPI のバリエーション**</span><span class="sxs-lookup"><span data-stu-id="681d7-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="681d7-125">インターフェイスメソッドのすべての文字列パラメーターは Unicode にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="681d7-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="681d7-126">MAPI インターフェイスは、Unicode または ANSI 文字列パラメーターのいずれかを許可するように定義されています。</span><span class="sxs-lookup"><span data-stu-id="681d7-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="681d7-127">文字列パラメーターを持つ多くのメソッドに**ulflags**パラメーターも指定されています。文字列パラメータの幅は、 **ulflags**の MAPI_UNICODE フラグの値で示されます。</span><span class="sxs-lookup"><span data-stu-id="681d7-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="681d7-128">一部の MAPI インターフェイスは、Unicode をサポートしておらず、MAPI_UNICODE フラグが設定されている場合は MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="681d7-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="681d7-129">すべてのインターフェイスメソッドには、戻り値の型が HRESULT である必要があります。</span><span class="sxs-lookup"><span data-stu-id="681d7-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="681d7-130">MAPI には、HRESULT でない値: [IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)を返すメソッドが少なくとも1つあります。</span><span class="sxs-lookup"><span data-stu-id="681d7-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="681d7-131">呼び出し元と実装者は、標準の COM タスク allocators を使用して、インターフェイスパラメーターのメモリを割り当てて解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="681d7-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="681d7-132">すべての MAPI メソッドは、リンクされた allocators [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)を使用して、インターフェイスパラメーターのメモリを管理します。</span><span class="sxs-lookup"><span data-stu-id="681d7-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="681d7-133">[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)など、OLE によって定義されたインターフェイスのすべての MAPI 実装は、標準の COM タスク allocators を使用します。</span><span class="sxs-lookup"><span data-stu-id="681d7-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="681d7-134">メソッドが失敗した場合は、すべての out ポインターパラメーターを明示的に NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="681d7-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="681d7-135">MAPI インターフェイスでは、out ポインターパラメーターを NULL に設定するか、またはメソッドが失敗した場合は変更しないままにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="681d7-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="681d7-136">OLE によって定義されたインターフェイスのすべての MAPI 実装は、失敗時にパラメーターを NULL に明示的に設定します。</span><span class="sxs-lookup"><span data-stu-id="681d7-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="681d7-137">可能な限り、集約可能なオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="681d7-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="681d7-138">MAPI インターフェイスは集約できません。</span><span class="sxs-lookup"><span data-stu-id="681d7-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="681d7-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="681d7-139">See also</span></span>



[<span data-ttu-id="681d7-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="681d7-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="681d7-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="681d7-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="681d7-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="681d7-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="681d7-143">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="681d7-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

