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
# <a name="msproviderinit"></a><span data-ttu-id="ecf1a-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="ecf1a-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="ecf1a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecf1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecf1a-105">操作用にメッセージ ストア プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecf1a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ecf1a-106">Header file:</span></span>  <br/> |<span data-ttu-id="ecf1a-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ecf1a-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ecf1a-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ecf1a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ecf1a-109">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ecf1a-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="ecf1a-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ecf1a-110">Called by:</span></span>  <br/> |<span data-ttu-id="ecf1a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ecf1a-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ecf1a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ecf1a-112">Parameters</span></span>

 <span data-ttu-id="ecf1a-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-113">_hInstance_</span></span>
  
> <span data-ttu-id="ecf1a-114">[in]MAPI がリンク時に使用したメッセージ ストア プロバイダーのダイナミック リンク ライブラリ (DLL) のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="ecf1a-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="ecf1a-116">[in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="ecf1a-117">メッセージ ストア プロバイダーは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="ecf1a-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="ecf1a-119">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="ecf1a-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="ecf1a-121">[in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="ecf1a-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="ecf1a-123">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="ecf1a-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-124">_ulFlags_</span></span>
  
> <span data-ttu-id="ecf1a-125">[in]フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="ecf1a-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-126">The following flag can be set:</span></span>
    
<span data-ttu-id="ecf1a-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="ecf1a-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="ecf1a-128">プロバイダーは、ユーザー インターフェイスにアクセスすることなく、Windowsサービスのコンテキストで読み込まれています。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="ecf1a-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="ecf1a-130">[in]MAPI が使用するサービス プロバイダー インターフェイス (SPI) のバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="ecf1a-131">現在のバージョン番号については、Mapispi.h ヘッダー ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="ecf1a-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="ecf1a-133">[out]このメッセージ ストア プロバイダーが使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="ecf1a-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="ecf1a-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="ecf1a-135">[out]初期化されたメッセージ ストア プロバイダー オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ecf1a-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="ecf1a-136">Return value</span></span>

<span data-ttu-id="ecf1a-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="ecf1a-137">S_OK</span></span> 
  
> <span data-ttu-id="ecf1a-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ecf1a-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="ecf1a-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="ecf1a-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="ecf1a-140">MAPI で使用されている SPI バージョンは、このプロバイダーで使用されている SPI と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecf1a-141">注釈</span><span class="sxs-lookup"><span data-stu-id="ecf1a-141">Remarks</span></span>

<span data-ttu-id="ecf1a-142">MAPI は、エントリ ポイント関数 **MSProviderInit** を呼び出して、クライアント ログオン後にメッセージ ストア プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ecf1a-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="ecf1a-143">Notes to implementers</span></span>

<span data-ttu-id="ecf1a-144">メッセージ ストア プロバイダーは、プロバイダーの DLL のエントリ ポイント関数として **MSProviderInit** を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="ecf1a-145">実装は **、MAPISPI.H でも指定されている MSPROVIDERINIT** 関数プロトタイプに基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="ecf1a-146">MAPI では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用する **MSPROVIDERINIT** が定義されています。この場合 **、MSProviderInit** は CDECL 呼び出し規約に従います。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="ecf1a-147">CDECL の利点は、呼び出しパラメーターの数が定義されたパラメーターの数と一致しない場合でも、呼び出しを試行できる点です。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="ecf1a-148">同時に複数のプロファイルに表示された結果、または同じプロファイルに複数回表示された結果として、プロバイダーを複数回初期化できます。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="ecf1a-149">プロバイダー オブジェクトにはコンテキストが含まれているため **、MSProviderInit** は、同じプロセスで複数の初期化を行う場合でも、初期化ごとに  _lppMSProvider_ 内の別のプロバイダー オブジェクトを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="ecf1a-150">プロバイダー DLL は、プロバイダー DLL とリンクMapix.dll。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="ecf1a-151">代わりに、メモリ割り当てまたは割り当て解除にこれらのポインターを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="ecf1a-152">メッセージ ストア プロバイダーは、ほとんどのメモリ割り当てと割り当て解除のために _、lpAllocateBuffer_ _、lpAllocateMore、__および lpFreeBuffer_ が指す関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="ecf1a-153">特に、 [プロバイダーは、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てるには、これらの関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="ecf1a-154">プロバイダーが OLE メモリ アロケーターを使用する場合は _、lpMalloc_ パラメーターが指すアロケーター オブジェクトの **IUnknown::AddRef** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="ecf1a-155">**MSProviderInit の記述の詳細については、「メッセージ** ストア プロバイダーの読み込 [み」を参照してください](loading-message-store-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="ecf1a-156">エントリ ポイント関数の詳細については、「Service Provider Entry Point Function の [実装」を参照してください](implementing-a-service-provider-entry-point-function.md)。</span><span class="sxs-lookup"><span data-stu-id="ecf1a-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ecf1a-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecf1a-157">See also</span></span>



[<span data-ttu-id="ecf1a-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="ecf1a-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="ecf1a-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecf1a-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="ecf1a-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="ecf1a-160">XPProviderInit</span></span>](xpproviderinit.md)

