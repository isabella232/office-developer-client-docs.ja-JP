---
title: コンポーネント オブジェクト モデルと MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334469"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="fcd60-103">コンポーネント オブジェクト モデルと MAPI</span><span class="sxs-lookup"><span data-stu-id="fcd60-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="fcd60-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcd60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcd60-105">SDK Windowsドキュメントには、コンポーネント オブジェクト モデル (COM) に準拠するオブジェクトを実装するためのルールの包括的な説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fcd60-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="fcd60-106">これらのルールは、次の方法に対処します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="fcd60-107">インターフェイスとオブジェクトを設計します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="fcd60-108">[IUnknown インターフェイスを実装](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="fcd60-109">メモリを管理します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-109">Manage memory.</span></span>
    
- <span data-ttu-id="fcd60-110">参照カウントを処理します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="fcd60-111">アパートメント スレッド オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="fcd60-112">すべての MAPI オブジェクトは [、IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)から継承するインターフェイスを実装するために COM ベースと見なされますが、MAPI は一部の状況では標準の COM ルールから離れる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fcd60-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="fcd60-113">このずれにより、開発者は実装の柔軟性を高める可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fcd60-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="fcd60-114">たとえば、MAPI インターフェイスは、任意の COM インターフェイスと同様に、実装者と呼び出し元の間のコントラクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="fcd60-115">インターフェイスを作成して公開すると、その定義は変更できません。変更されません。</span><span class="sxs-lookup"><span data-stu-id="fcd60-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="fcd60-116">MAPI は、この説明から逸脱しないが、説明をややリラックスさせる。</span><span class="sxs-lookup"><span data-stu-id="fcd60-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="fcd60-117">実装者は、呼び出し元に次のいずれかのエラー値を返す、特定のメソッドを実装しない選択できます。</span><span class="sxs-lookup"><span data-stu-id="fcd60-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="fcd60-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="fcd60-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="fcd60-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="fcd60-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="fcd60-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fcd60-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="fcd60-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="fcd60-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="fcd60-122">標準 COM ルールからのその他の偏差については、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="fcd60-123">**COM プログラミング ルール**</span><span class="sxs-lookup"><span data-stu-id="fcd60-123">**COM programming rule**</span></span>|<span data-ttu-id="fcd60-124">**MAPI のバリエーション**</span><span class="sxs-lookup"><span data-stu-id="fcd60-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcd60-125">インターフェイス メソッドのすべての文字列パラメーターは Unicode である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcd60-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="fcd60-126">MAPI インターフェイスは、Unicode または ANSI 文字列パラメーターのいずれかを許可するために定義されます。</span><span class="sxs-lookup"><span data-stu-id="fcd60-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="fcd60-127">文字列パラメーターを持つ多くのメソッドにも **ulFlags パラメーター** があります。文字列パラメーター の幅は **、ulFlags** の MAPI_UNICODEの値で示されます。</span><span class="sxs-lookup"><span data-stu-id="fcd60-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="fcd60-128">MAPI インターフェイスの中には、Unicode をサポートしていないものMAPI_E_BAD_CHARWIDTHフラグが設定MAPI_UNICODE返されます。</span><span class="sxs-lookup"><span data-stu-id="fcd60-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="fcd60-129">すべてのインターフェイス メソッドには、HRESULT の戻り値の型が必要です。</span><span class="sxs-lookup"><span data-stu-id="fcd60-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="fcd60-130">MAPI には、HRESULT 以外の値を返す少なくとも 1 つのメソッドがあります [。IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)です。</span><span class="sxs-lookup"><span data-stu-id="fcd60-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="fcd60-131">呼び出し元と実装者は、標準の COM タスク アロケーターを使用して、インターフェイス パラメーターのメモリを割り当て、解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcd60-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="fcd60-132">すべての MAPI メソッドは、リンクされたアロケーター MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer を使用して、インターフェイス パラメーターのメモリを管理します。 [](mapiallocatebuffer.md) [](mapiallocatemore.md) [](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="fcd60-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="fcd60-133">[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)など、OLE によって定義されたインターフェイスのすべての MAPI 実装では、標準の COM タスク アロケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="fcd60-134">メソッドが失敗した場合は、すべてのアウト ポインター パラメーターを明示的に NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcd60-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="fcd60-135">MAPI インターフェイスでは、メソッドが失敗した場合、ポインター パラメーターを NULL に設定するか、変更しないままにしてください。</span><span class="sxs-lookup"><span data-stu-id="fcd60-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="fcd60-136">OLE によって定義されたインターフェイスのすべての MAPI 実装は、エラー時にパラメーターを NULL に明示的に設定します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="fcd60-137">可能な限り、aggregatable オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="fcd60-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="fcd60-138">MAPI インターフェイスは、アグリガテーブルではありません。</span><span class="sxs-lookup"><span data-stu-id="fcd60-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcd60-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcd60-139">See also</span></span>



[<span data-ttu-id="fcd60-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="fcd60-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="fcd60-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="fcd60-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="fcd60-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fcd60-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="fcd60-143">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="fcd60-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

