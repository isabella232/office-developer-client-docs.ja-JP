---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33adef7a8248e137869912afc2026583828b087e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570171"
---
# <a name="msproviderinit"></a><span data-ttu-id="b5301-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="b5301-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="b5301-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5301-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5301-105">操作のメッセージ ストア プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b5301-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5301-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b5301-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5301-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="b5301-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="b5301-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b5301-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b5301-109">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b5301-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="b5301-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b5301-110">Called by:</span></span>  <br/> |<span data-ttu-id="b5301-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b5301-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a><span data-ttu-id="b5301-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b5301-112">Parameters</span></span>

 <span data-ttu-id="b5301-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="b5301-113">_hInstance_</span></span>
  
> <span data-ttu-id="b5301-114">[in]メッセージのインスタンスは、それにリンクされている場合、MAPI が使用されるプロバイダーのダイナミック リンク ライブラリ (DLL) を格納します。</span><span class="sxs-lookup"><span data-stu-id="b5301-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="b5301-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="b5301-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="b5301-116">[in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5301-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="b5301-117">メッセージ ストア プロバイダーは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5301-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="b5301-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="b5301-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="b5301-119">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5301-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="b5301-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="b5301-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="b5301-121">[in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5301-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="b5301-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="b5301-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="b5301-123">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5301-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="b5301-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b5301-124">_ulFlags_</span></span>
  
> <span data-ttu-id="b5301-125">[in]フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="b5301-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="b5301-126">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b5301-126">The following flag can be set:</span></span>
    
<span data-ttu-id="b5301-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="b5301-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="b5301-128">プロバイダーは、Windows サービス、特別な種類のすべてのユーザー インターフェイスにアクセスすることがなくプロセスのコンテキストで行われます。</span><span class="sxs-lookup"><span data-stu-id="b5301-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="b5301-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="b5301-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="b5301-130">[in]MAPI を使用するサービス プロバイダー インターフェイス (SPI) のバージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="b5301-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="b5301-131">現在のバージョン番号は、Mapispi.h ヘッダー ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5301-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="b5301-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="b5301-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="b5301-133">[out]このメッセージ ストア プロバイダーを使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5301-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="b5301-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="b5301-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="b5301-135">[out]初期化メッセージ ストア プロバイダー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5301-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b5301-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b5301-136">Return value</span></span>

<span data-ttu-id="b5301-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5301-137">S_OK</span></span> 
  
> <span data-ttu-id="b5301-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b5301-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b5301-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="b5301-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="b5301-140">MAPI によって使用されている SPI のバージョンは、このプロバイダーで使用されている SPI との互換性ではありません。</span><span class="sxs-lookup"><span data-stu-id="b5301-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5301-141">注釈</span><span class="sxs-lookup"><span data-stu-id="b5301-141">Remarks</span></span>

<span data-ttu-id="b5301-142">MAPI は、クライアント ログオンの後、メッセージ ストア プロバイダーを初期化するために**MSProviderInit**エントリ ポイント関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b5301-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b5301-143">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="b5301-143">Notes to implementers</span></span>

<span data-ttu-id="b5301-144">メッセージ ストア プロバイダーは、プロバイダーの DLL にエントリ ポイント関数として**MSProviderInit**を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5301-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="b5301-145">実装は、 **MSPROVIDERINIT**関数のプロトタイプで指定されている MAPISPI もに基づいている必要があります。H.</span><span class="sxs-lookup"><span data-stu-id="b5301-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="b5301-146">MAPI では、型を使用する標準的な MAPI の初期化の呼び出し、CDECL 呼び出し規約に従う**MSProviderInit**を STDMAPIINITCALLTYPE、 **MSPROVIDERINIT**を定義します。</span><span class="sxs-lookup"><span data-stu-id="b5301-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="b5301-147">CDECL の利点は、呼び出しのパラメーターの数が定義されているパラメーターの数と一致しない場合でも呼び出しを試行することができます。</span><span class="sxs-lookup"><span data-stu-id="b5301-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="b5301-148">プロバイダーは、同時使用中、または同じプロファイルで複数回表示されるは、いくつかのプロファイルに表示されるため、複数回初期化できます。</span><span class="sxs-lookup"><span data-stu-id="b5301-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="b5301-149">プロバイダー オブジェクトには、コンテキストが含まれている、ため**MSProviderInit**ごとの初期化を同じプロセスで複数回初期化の場合でも_lppMSProvider_で、別のプロバイダー オブジェクトを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5301-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="b5301-150">Mapix.dll で、プロバイダーの DLL をリンクしないようにします。</span><span class="sxs-lookup"><span data-stu-id="b5301-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="b5301-151">代わりに、メモリの割り当てまたは割り当て解除用には、これらのポインターを使用してください。</span><span class="sxs-lookup"><span data-stu-id="b5301-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="b5301-152">メッセージ ストア プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと割り当て解除の_lpFreeBuffer_が指す関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5301-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="b5301-153">具体的には、プロバイダーでは、 [IMAPIProp::GetProps](imapiprop-getprops.md)や[IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当てにこれらの関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5301-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="b5301-154">プロバイダーは、OLE のメモリ アロケーターを使用しても期待しています、する場合は、 _lpMalloc_パラメーターで指定されたアロケーター オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b5301-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="b5301-155">**MSProviderInit**の作成方法の詳細については、[メッセージ ストア プロバイダーの読み込み](loading-message-store-providers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5301-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="b5301-156">エントリ ポイント関数の詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5301-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5301-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5301-157">See also</span></span>



[<span data-ttu-id="b5301-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="b5301-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="b5301-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5301-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="b5301-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="b5301-160">XPProviderInit</span></span>](xpproviderinit.md)

