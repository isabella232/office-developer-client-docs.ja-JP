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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 38b60180ae7c417bf34998e72f96b353ace02859
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592536"
---
# <a name="xpproviderinit"></a><span data-ttu-id="a9a23-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="a9a23-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="a9a23-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9a23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9a23-105">操作のためのトランスポート プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a9a23-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9a23-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a9a23-106">Header file:</span></span>  <br/> |<span data-ttu-id="a9a23-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a9a23-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a9a23-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a9a23-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a9a23-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="a9a23-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-110">Called by:</span></span>  <br/> |<span data-ttu-id="a9a23-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a9a23-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a9a23-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a9a23-112">Parameters</span></span>

 <span data-ttu-id="a9a23-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="a9a23-113">_hInstance_</span></span>
  
> <span data-ttu-id="a9a23-114">[in]DLL が読み込まれるときに使用されるトランスポート プロバイダーのダイナミック リンク ライブラリ (DLL)、MAPI のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="a9a23-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="a9a23-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="a9a23-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="a9a23-116">[in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9a23-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="a9a23-117">トランスポート プロバイダーは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9a23-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="a9a23-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="a9a23-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a9a23-119">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9a23-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="a9a23-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="a9a23-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="a9a23-121">[in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9a23-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="a9a23-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="a9a23-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="a9a23-123">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9a23-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="a9a23-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9a23-124">_ulFlags_</span></span>
  
> <span data-ttu-id="a9a23-125">[in]フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a9a23-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="a9a23-126">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-126">The following flag can be set:</span></span>
    
<span data-ttu-id="a9a23-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="a9a23-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="a9a23-128">プロバイダーは、Windows サービス、特別な種類のすべてのユーザー インターフェイスにアクセスすることがなくプロセスのコンテキストで行われます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="a9a23-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="a9a23-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="a9a23-130">[in]Mapi.dll を使用するサービス プロバイダー インターフェイス (SPI) のバージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="a9a23-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="a9a23-131">現在のバージョン番号は、Mapispi.h ヘッダー ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9a23-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="a9a23-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="a9a23-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="a9a23-133">[out]このトランスポート プロバイダーを使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9a23-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="a9a23-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="a9a23-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="a9a23-135">[out]初期化されたトランスポート プロバイダー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9a23-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a9a23-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a9a23-136">Return value</span></span>

<span data-ttu-id="a9a23-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9a23-137">S_OK</span></span> 
  
> <span data-ttu-id="a9a23-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a9a23-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a9a23-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="a9a23-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="a9a23-140">MAPI によって使用されている SPI のバージョンは、このプロバイダーで使用されている SPI との互換性ではありません。</span><span class="sxs-lookup"><span data-stu-id="a9a23-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9a23-141">注釈</span><span class="sxs-lookup"><span data-stu-id="a9a23-141">Remarks</span></span>

<span data-ttu-id="a9a23-142">MAPI は、クライアント ログオンを次のトランスポート プロバイダーを初期化するために**XPProviderInit**エントリ ポイント関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="a9a23-143">**XPProviderInit**は、クライアントのプロファイルで指定されたトランスポート プロバイダーごとに 1 回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a9a23-144">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="a9a23-144">Notes to implementers</span></span>

<span data-ttu-id="a9a23-145">トランスポート プロバイダーは、プロバイダーの DLL にエントリ ポイント関数として**XPProviderInit**を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9a23-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="a9a23-146">実装は、 **XPPROVIDERINIT**関数のプロトタイプで指定されている Mapispi.h もに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9a23-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="a9a23-147">MAPI では、型を使用する標準的な MAPI の初期化の呼び出し、CDECL 呼び出し規約に従う**XPProviderInit**を STDMAPIINITCALLTYPE、 **XPPROVIDERINIT**を定義します。</span><span class="sxs-lookup"><span data-stu-id="a9a23-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="a9a23-148">CDECL の利点は、呼び出しのパラメーターの数が定義されているパラメーターの数と一致しない場合でも呼び出しを試行することができます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="a9a23-149">同時使用中、または同じプロファイルで複数回表示されるは、いくつかのプロファイルに表示される結果として、プロバイダーを複数回初期化できます。</span><span class="sxs-lookup"><span data-stu-id="a9a23-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="a9a23-150">プロバイダー オブジェクトには、コンテキストが含まれている、ため**XPProviderInit**ごとの初期化を同じプロセスで複数回初期化の場合でも_lppXPProvider_で、別のプロバイダー オブジェクトを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9a23-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="a9a23-151">トランスポート プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと割り当て解除の_lpFreeBuffer_が指す関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9a23-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="a9a23-152">具体的には、プロバイダーでは、 [IMAPIProp::GetProps](imapiprop-getprops.md)や[IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当てにこれらの関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9a23-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="a9a23-153">プロバイダーは、OLE のメモリ アロケーターを使用しても期待しています、する場合は、 _lpMalloc_パラメーターで指定されたアロケーター オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9a23-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="a9a23-154">**XPProviderInit**の作成方法の詳細については、[トランスポート プロバイダーの初期化](initializing-the-transport-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9a23-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="a9a23-155">エントリ ポイント関数の詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9a23-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9a23-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9a23-156">See also</span></span>



[<span data-ttu-id="a9a23-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="a9a23-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="a9a23-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9a23-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="a9a23-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="a9a23-159">MSProviderInit</span></span>](msproviderinit.md)

