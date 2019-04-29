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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416238"
---
# <a name="msproviderinit"></a><span data-ttu-id="6655f-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="6655f-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="6655f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6655f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6655f-105">操作用のメッセージストアプロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6655f-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6655f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6655f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6655f-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="6655f-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="6655f-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6655f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6655f-109">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="6655f-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="6655f-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6655f-110">Called by:</span></span>  <br/> |<span data-ttu-id="6655f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6655f-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6655f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6655f-112">Parameters</span></span>

 <span data-ttu-id="6655f-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="6655f-113">_hInstance_</span></span>
  
> <span data-ttu-id="6655f-114">順番MAPI がリンクしたときに使用したメッセージストアプロバイダーのダイナミックリンクライブラリ (DLL) のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="6655f-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="6655f-115">_lpmalloc_</span><span class="sxs-lookup"><span data-stu-id="6655f-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="6655f-116">順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6655f-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="6655f-117">メッセージストアプロバイダーは、 **IStream**など特定のインターフェイスを使用するときに、この割り当て方法を使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="6655f-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="6655f-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="6655f-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="6655f-119">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6655f-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="6655f-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="6655f-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="6655f-121">順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6655f-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="6655f-122">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="6655f-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="6655f-123">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6655f-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="6655f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6655f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="6655f-125">順番フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="6655f-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="6655f-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6655f-126">The following flag can be set:</span></span>
    
<span data-ttu-id="6655f-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="6655f-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="6655f-128">プロバイダーは、ユーザーインターフェイスにアクセスできない特別な種類のプロセスである Windows サービスのコンテキストに読み込まれています。</span><span class="sxs-lookup"><span data-stu-id="6655f-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="6655f-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="6655f-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="6655f-130">順番MAPI が使用するサービスプロバイダインターフェイス (SPI) のバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="6655f-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="6655f-131">現在のバージョン番号については、Mapispi ヘッダーファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6655f-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="6655f-132">_lアウト providerver_</span><span class="sxs-lookup"><span data-stu-id="6655f-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="6655f-133">読み上げこのメッセージストアプロバイダーが使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6655f-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="6655f-134">_lppmsprovider_</span><span class="sxs-lookup"><span data-stu-id="6655f-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="6655f-135">読み上げ初期化されたメッセージストアプロバイダオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6655f-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6655f-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="6655f-136">Return value</span></span>

<span data-ttu-id="6655f-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="6655f-137">S_OK</span></span> 
  
> <span data-ttu-id="6655f-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6655f-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6655f-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="6655f-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="6655f-140">MAPI で使用されている spi バージョンは、このプロバイダーで使用されている spi と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="6655f-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6655f-141">注釈</span><span class="sxs-lookup"><span data-stu-id="6655f-141">Remarks</span></span>

<span data-ttu-id="6655f-142">MAPI はエントリポイント関数**msproviderinit**を呼び出して、クライアントログオンの後にメッセージストアプロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6655f-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6655f-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="6655f-143">Notes to implementers</span></span>

<span data-ttu-id="6655f-144">メッセージストアプロバイダーは、プロバイダーの DLL で**msproviderinit**をエントリポイント関数として実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6655f-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="6655f-145">この実装は、MAPISPI でも指定されている**msproviderinit**関数プロトタイプに基づいている必要があります。H.</span><span class="sxs-lookup"><span data-stu-id="6655f-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="6655f-146">mapi は、 **msproviderinit**を定義して、標準の mapi 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用します。これにより、 **msproviderinit**は CDECL の呼び出し規則に従います。</span><span class="sxs-lookup"><span data-stu-id="6655f-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="6655f-147">CDECL の利点は、呼び出し元のパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できることです。</span><span class="sxs-lookup"><span data-stu-id="6655f-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="6655f-148">プロバイダーは、複数のプロファイルに同時に使用された結果、または同じプロファイルに複数回出現した結果として、複数回初期化することができます。</span><span class="sxs-lookup"><span data-stu-id="6655f-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="6655f-149">プロバイダーオブジェクトにはコンテキストが含まれているため、 **msproviderinit**は、同じプロセス内で複数の初期化があっても、各初期化に対して_lppmsprovider_の異なるプロバイダーオブジェクトを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6655f-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="6655f-150">プロバイダー DLL は、mapix にリンクしてはなりません。</span><span class="sxs-lookup"><span data-stu-id="6655f-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="6655f-151">代わりに、これらのポインターを使用してメモリの割り当てまたは割り当てを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6655f-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="6655f-152">メッセージストアプロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、ほとんどのメモリの割り当てと割り当てを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6655f-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="6655f-153">特に、プロバイダーはこれらの関数を使用して、 [imapiprop:: GetProps](imapiprop-getprops.md) 、 [IMAPITable:: QueryRows](imapitable-queryrows.md)などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6655f-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="6655f-154">プロバイダーが OLE メモリアロケーターを使用することを前提としている場合は、 _lpmalloc_パラメーターで指定されたアロケーターオブジェクトの**IUnknown:: AddRef**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6655f-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="6655f-155">**msproviderinit**の記述の詳細については、「[メッセージストアプロバイダーの読み込み](loading-message-store-providers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6655f-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="6655f-156">エントリポイント関数の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6655f-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6655f-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="6655f-157">See also</span></span>



[<span data-ttu-id="6655f-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="6655f-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="6655f-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6655f-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="6655f-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="6655f-160">XPProviderInit</span></span>](xpproviderinit.md)

