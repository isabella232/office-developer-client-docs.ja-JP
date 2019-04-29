---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428537"
---
# <a name="xpproviderinit"></a><span data-ttu-id="37d3d-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="37d3d-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="37d3d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37d3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37d3d-105">操作のためにトランスポートプロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="37d3d-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37d3d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="37d3d-106">Header file:</span></span>  <br/> |<span data-ttu-id="37d3d-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="37d3d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="37d3d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="37d3d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="37d3d-109">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="37d3d-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="37d3d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="37d3d-110">Called by:</span></span>  <br/> |<span data-ttu-id="37d3d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="37d3d-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a><span data-ttu-id="37d3d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37d3d-112">Parameters</span></span>

 <span data-ttu-id="37d3d-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="37d3d-113">_hInstance_</span></span>
  
> <span data-ttu-id="37d3d-114">順番dll を読み込んだときに MAPI が使用するトランスポートプロバイダーのダイナミックリンクライブラリ (dll) のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="37d3d-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="37d3d-115">_lpmalloc_</span><span class="sxs-lookup"><span data-stu-id="37d3d-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="37d3d-116">順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37d3d-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="37d3d-117">**IStream**などの特定のインターフェイスを使用する場合、トランスポートプロバイダーはこの allocation メソッドを使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="37d3d-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="37d3d-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="37d3d-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="37d3d-119">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37d3d-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="37d3d-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="37d3d-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="37d3d-121">順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37d3d-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="37d3d-122">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="37d3d-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="37d3d-123">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37d3d-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="37d3d-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37d3d-124">_ulFlags_</span></span>
  
> <span data-ttu-id="37d3d-125">順番フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="37d3d-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="37d3d-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="37d3d-126">The following flag can be set:</span></span>
    
<span data-ttu-id="37d3d-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="37d3d-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="37d3d-128">プロバイダーは、ユーザーインターフェイスにアクセスできない特別な種類のプロセスである Windows サービスのコンテキストに読み込まれています。</span><span class="sxs-lookup"><span data-stu-id="37d3d-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="37d3d-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="37d3d-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="37d3d-130">順番Mapi .dll が使用するサービスプロバイダインターフェイス (SPI) のバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="37d3d-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="37d3d-131">現在のバージョン番号については、Mapispi ヘッダーファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d3d-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="37d3d-132">_lアウト providerver_</span><span class="sxs-lookup"><span data-stu-id="37d3d-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="37d3d-133">読み上げこのトランスポートプロバイダーが使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37d3d-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="37d3d-134">_lppxps プロバイダ_</span><span class="sxs-lookup"><span data-stu-id="37d3d-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="37d3d-135">読み上げ初期化されたトランスポートプロバイダオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37d3d-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37d3d-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="37d3d-136">Return value</span></span>

<span data-ttu-id="37d3d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="37d3d-137">S_OK</span></span> 
  
> <span data-ttu-id="37d3d-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="37d3d-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="37d3d-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="37d3d-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="37d3d-140">MAPI で使用されている spi バージョンは、このプロバイダーで使用されている spi と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="37d3d-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37d3d-141">注釈</span><span class="sxs-lookup"><span data-stu-id="37d3d-141">Remarks</span></span>

<span data-ttu-id="37d3d-142">MAPI は、クライアントログオンの後にトランスポートプロバイダーを初期化するために、エントリポイント関数の**xps providerinit**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="37d3d-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="37d3d-143">クライアントのプロファイルに指定されている各トランスポートプロバイダーに対して、 **xps providerinit**が1回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="37d3d-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="37d3d-144">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="37d3d-144">Notes to implementers</span></span>

<span data-ttu-id="37d3d-145">トランスポートプロバイダーは、プロバイダーの DLL で、エントリポイント関数として、 **xps providerinit**を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d3d-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="37d3d-146">この実装は、Mapispi でも指定されている、 **xps の init**関数プロトタイプに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d3d-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="37d3d-147">mapi では、STDMAPIINITCALLTYPE という標準の MAPI 初期化呼び出しの種類であるを使用するように、 **xps の init**が定義されています。これにより、 **xps の init**は CDECL の呼び出し規則に従います。</span><span class="sxs-lookup"><span data-stu-id="37d3d-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="37d3d-148">CDECL の利点は、呼び出し元のパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できることです。</span><span class="sxs-lookup"><span data-stu-id="37d3d-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="37d3d-149">プロバイダーは、複数のプロファイルに同時に表示された結果、または同じプロファイルに複数回出現した結果として、複数回初期化することができます。</span><span class="sxs-lookup"><span data-stu-id="37d3d-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="37d3d-150">プロバイダーオブジェクトにはコンテキストが含まれているため、同じプロセス内で複数の初期化があっても、各初期化に対して、 **xps providerinit**は別のプロバイダーオブジェクトを_lppxps プロバイダー_で返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d3d-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="37d3d-151">トランスポートプロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、ほとんどのメモリの割り当てと割り当てを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d3d-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="37d3d-152">特に、プロバイダーはこれらの関数を使用して、 [imapiprop:: GetProps](imapiprop-getprops.md) 、 [IMAPITable:: QueryRows](imapitable-queryrows.md)などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d3d-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="37d3d-153">プロバイダーが OLE メモリアロケーターを使用することを前提としている場合は、 _lpmalloc_パラメーターで指定されたアロケーターオブジェクトの**IUnknown:: AddRef**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d3d-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="37d3d-154">**xp の init**の記述の詳細については、「[トランスポートプロバイダーの初期化](initializing-the-transport-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d3d-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="37d3d-155">エントリポイント関数の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d3d-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37d3d-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="37d3d-156">See also</span></span>



[<span data-ttu-id="37d3d-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="37d3d-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="37d3d-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37d3d-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="37d3d-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="37d3d-159">MSProviderInit</span></span>](msproviderinit.md)

