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
# <a name="xpproviderinit"></a><span data-ttu-id="cd1b0-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="cd1b0-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="cd1b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd1b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd1b0-105">操作用にトランスポート プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd1b0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cd1b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd1b0-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="cd1b0-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="cd1b0-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="cd1b0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd1b0-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cd1b0-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="cd1b0-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="cd1b0-110">Called by:</span></span>  <br/> |<span data-ttu-id="cd1b0-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="cd1b0-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="cd1b0-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd1b0-112">Parameters</span></span>

 <span data-ttu-id="cd1b0-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-113">_hInstance_</span></span>
  
> <span data-ttu-id="cd1b0-114">[in]MAPI が DLL の読み込み時に使用したトランスポート プロバイダーのダイナミック リンク ライブラリ (DLL) のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="cd1b0-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="cd1b0-116">[in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="cd1b0-117">トランスポート プロバイダーは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="cd1b0-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="cd1b0-119">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="cd1b0-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="cd1b0-121">[in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="cd1b0-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="cd1b0-123">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="cd1b0-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-124">_ulFlags_</span></span>
  
> <span data-ttu-id="cd1b0-125">[in]フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="cd1b0-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-126">The following flag can be set:</span></span>
    
<span data-ttu-id="cd1b0-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="cd1b0-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="cd1b0-128">プロバイダーは、ユーザー インターフェイスにアクセスすることなく、Windowsサービスのコンテキストで読み込まれています。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="cd1b0-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="cd1b0-130">[in]ユーザーが使用するサービス プロバイダー インターフェイス (SPI) Mapi.dll番号。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="cd1b0-131">現在のバージョン番号については、Mapispi.h ヘッダー ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="cd1b0-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="cd1b0-133">[out]このトランスポート プロバイダーが使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="cd1b0-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="cd1b0-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="cd1b0-135">[out]初期化されたトランスポート プロバイダー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cd1b0-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="cd1b0-136">Return value</span></span>

<span data-ttu-id="cd1b0-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd1b0-137">S_OK</span></span> 
  
> <span data-ttu-id="cd1b0-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="cd1b0-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="cd1b0-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="cd1b0-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="cd1b0-140">MAPI で使用されている SPI バージョンは、このプロバイダーで使用されている SPI と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd1b0-141">注釈</span><span class="sxs-lookup"><span data-stu-id="cd1b0-141">Remarks</span></span>

<span data-ttu-id="cd1b0-142">MAPI は、エントリ ポイント関数 **XPProviderInit** を呼び出して、クライアント ログオン後にトランスポート プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="cd1b0-143">**XPProviderInit は** 、クライアントのプロファイルで指定されたトランスポート プロバイダーごとに 1 回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cd1b0-144">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="cd1b0-144">Notes to implementers</span></span>

<span data-ttu-id="cd1b0-145">トランスポート プロバイダーは、プロバイダーの DLL のエントリ ポイント関数として **XPProviderInit** を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="cd1b0-146">実装は **、Mapispi.h でも指定された XPPROVIDERINIT** 関数プロトタイプに基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="cd1b0-147">MAPI では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用する **XPPROVIDERINIT** が定義されています。この場合 **、XPProviderInit** は CDECL 呼び出し規約に従います。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="cd1b0-148">CDECL の利点は、呼び出しパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できる点です。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="cd1b0-149">同時に複数のプロファイルに表示された結果、または同じプロファイルに複数回表示された結果として、プロバイダーを複数回初期化できます。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="cd1b0-150">プロバイダー オブジェクトにはコンテキストが含まれているため **、XPProviderInit** は、同じプロセスで複数の初期化を行う場合でも、初期化ごとに  _lppXPProvider_ 内の別のプロバイダー オブジェクトを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="cd1b0-151">トランスポート プロバイダーは、ほとんどのメモリ割り当てと割り当て解除のために _、lpAllocateBuffer_ _、lpAllocateMore、__および lpFreeBuffer_ が指す関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="cd1b0-152">特に、 [プロバイダーは、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てるには、これらの関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="cd1b0-153">プロバイダーが OLE メモリ アロケーターを使用する場合は _、lpMalloc_ パラメーターが指すアロケーター オブジェクトの **IUnknown::AddRef** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="cd1b0-154">**XPProviderInit の記述の詳細については、「トランスポート** プロバイダーの [初期化」を参照してください](initializing-the-transport-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="cd1b0-155">エントリ ポイント関数の詳細については、「Service Provider Entry Point Function の [実装」を参照してください](implementing-a-service-provider-entry-point-function.md)。</span><span class="sxs-lookup"><span data-stu-id="cd1b0-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd1b0-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd1b0-156">See also</span></span>



[<span data-ttu-id="cd1b0-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="cd1b0-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="cd1b0-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd1b0-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="cd1b0-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="cd1b0-159">MSProviderInit</span></span>](msproviderinit.md)

