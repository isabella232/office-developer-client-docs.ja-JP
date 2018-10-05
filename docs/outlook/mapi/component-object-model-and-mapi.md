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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394119"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="016f2-103">コンポーネント オブジェクト モデルと MAPI</span><span class="sxs-lookup"><span data-stu-id="016f2-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="016f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="016f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="016f2-105">Windows SDK ドキュメントには、コンポーネント オブジェクト モデル (COM) に準拠しているオブジェクトを実装するための規則の包括的な説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="016f2-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="016f2-106">これらの規則は、以下を実行する方法を対処します。</span><span class="sxs-lookup"><span data-stu-id="016f2-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="016f2-107">インターフェイスとオブジェクトを設計します。</span><span class="sxs-lookup"><span data-stu-id="016f2-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="016f2-108">[IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="016f2-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="016f2-109">メモリを管理します。</span><span class="sxs-lookup"><span data-stu-id="016f2-109">Manage memory.</span></span>
    
- <span data-ttu-id="016f2-110">参照カウントを処理します。</span><span class="sxs-lookup"><span data-stu-id="016f2-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="016f2-111">アパートメント スレッド オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="016f2-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="016f2-112">すべての MAPI オブジェクトと見なされます com [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)から継承するインターフェイスを実装するため、MAPI は、状況によっては標準の COM の規則からの逸脱します。</span><span class="sxs-lookup"><span data-stu-id="016f2-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="016f2-113">この偏差から、開発者は、実装でより柔軟にすることができます。</span><span class="sxs-lookup"><span data-stu-id="016f2-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="016f2-114">などの任意の COM インターフェイスと同様に、MAPI インターフェイスでは、作成者と呼び出し元のコントラクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="016f2-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="016f2-115">インタ フェースが作成され、公開、その定義はことはできず、変更されません。</span><span class="sxs-lookup"><span data-stu-id="016f2-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="016f2-116">この説明では、MAPI が外れていないが、説明を多少緩和します。</span><span class="sxs-lookup"><span data-stu-id="016f2-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="016f2-117">実装では特定のメソッドを実装するのにはエラー値は次のいずれかを呼び出し元に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="016f2-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="016f2-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="016f2-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="016f2-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="016f2-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="016f2-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="016f2-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="016f2-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="016f2-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="016f2-122">標準の COM の規則からの偏差は、次の表に説明します。</span><span class="sxs-lookup"><span data-stu-id="016f2-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="016f2-123">**COM プログラミングの規則**</span><span class="sxs-lookup"><span data-stu-id="016f2-123">**COM programming rule**</span></span>|<span data-ttu-id="016f2-124">**MAPI のバリエーション**</span><span class="sxs-lookup"><span data-stu-id="016f2-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="016f2-125">インターフェイスのメソッド内のすべての文字列パラメーターには、Unicode をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="016f2-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="016f2-126">MAPI インターフェイスは、Unicode または ANSI のいずれかの文字列パラメーターを許可するように定義されます。</span><span class="sxs-lookup"><span data-stu-id="016f2-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="016f2-127">文字列パラメーターをとるメソッドの多くもパラメーターを持つ、 **ulFlags**です。**ulFlags**に MAPI_UNICODE フラグの値の文字列パラメーターの幅が表示されます。</span><span class="sxs-lookup"><span data-stu-id="016f2-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="016f2-128">一部の MAPI インターフェイスをサポートしない Unicode MAPI_UNICODE フラグが設定されている場合は、MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="016f2-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="016f2-129">すべてのインターフェイス メソッドは、HRESULT の戻り値の型が必要です。</span><span class="sxs-lookup"><span data-stu-id="016f2-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="016f2-130">MAPI 以外の HRESULT 値を返すには、少なくとも 1 つのメソッドを持つ: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)。</span><span class="sxs-lookup"><span data-stu-id="016f2-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="016f2-131">呼び出し元および実装する必要があります解放し、メモリ インタ フェースのパラメーターの標準的な COM タスク アロケーターを使用しています。</span><span class="sxs-lookup"><span data-stu-id="016f2-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="016f2-132">MAPI のすべてのメソッドは、インターフェイスのパラメーター用のメモリを管理するために[MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)は、リンクされたアロケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="016f2-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="016f2-133">[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)など、OLE によって定義されたインターフェイスのすべての MAPI 実装では、標準的な COM タスク アロケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="016f2-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="016f2-134">すべてのポインター パラメーターする必要があります明示的に設定する NULL にメソッドが失敗したとき。</span><span class="sxs-lookup"><span data-stu-id="016f2-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="016f2-135">MAPI インターフェイスでは、ポインター パラメーターを NULL に設定または変更しないままメソッドを配置するかを失敗する必要があります。</span><span class="sxs-lookup"><span data-stu-id="016f2-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="016f2-136">OLE によって明示的に定義されているインタ フェースのすべての MAPI 実装では、失敗した場合に null パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="016f2-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="016f2-137">可能な限り、集約可能オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="016f2-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="016f2-138">MAPI インターフェイスは、集約可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="016f2-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="016f2-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="016f2-139">See also</span></span>



[<span data-ttu-id="016f2-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="016f2-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="016f2-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="016f2-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="016f2-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="016f2-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="016f2-143">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="016f2-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

