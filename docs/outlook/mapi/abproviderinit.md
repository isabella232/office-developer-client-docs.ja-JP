---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428285"
---
# <a name="abproviderinit"></a><span data-ttu-id="03923-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="03923-103">ABProviderInit</span></span>
 
<span data-ttu-id="03923-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03923-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03923-105">操作用にアドレス帳プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="03923-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03923-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="03923-106">Header file:</span></span>  <br/> |<span data-ttu-id="03923-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="03923-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="03923-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="03923-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="03923-109">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="03923-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="03923-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="03923-110">Called by:</span></span>  <br/> |<span data-ttu-id="03923-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="03923-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a><span data-ttu-id="03923-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="03923-112">Parameters</span></span>

 <span data-ttu-id="03923-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="03923-113">_hInstance_</span></span>
  
> <span data-ttu-id="03923-114">[in]MAPI がリンク時に使用したアドレス帳プロバイダーの動的リンク ライブラリ (DLL) のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="03923-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="03923-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="03923-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="03923-116">[in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="03923-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="03923-117">アドレス帳プロバイダーは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。</span><span class="sxs-lookup"><span data-stu-id="03923-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="03923-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="03923-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="03923-119">[in]MAPI がメモリを割り当てる必要がある場合に使用する [MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="03923-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="03923-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="03923-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="03923-121">[in] [MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。MAPI が追加のメモリを割り当てる必要がある場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="03923-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="03923-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="03923-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="03923-123">[in] [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。MAPI がメモリを解放するために必要な場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="03923-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="03923-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03923-124">_ulFlags_</span></span>
  
> <span data-ttu-id="03923-125">[in]フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="03923-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="03923-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="03923-126">The following flag can be set:</span></span>
    
<span data-ttu-id="03923-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="03923-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="03923-128">プロバイダーは、ユーザー インターフェイスにアクセスすることなく、Windowsサービスのコンテキストで読み込まれています。</span><span class="sxs-lookup"><span data-stu-id="03923-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="03923-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="03923-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="03923-130">[in]ユーザーが使用するサービス プロバイダー インターフェイス (SPI) MAPI.DLL番号。</span><span class="sxs-lookup"><span data-stu-id="03923-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="03923-131">現在のバージョン番号については、MAPISPI を参照してください。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="03923-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="03923-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="03923-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="03923-133">[out]このアドレス帳プロバイダーが使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="03923-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="03923-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="03923-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="03923-135">[out]初期化されたアドレス帳プロバイダー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="03923-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03923-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="03923-136">Return value</span></span>

<span data-ttu-id="03923-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="03923-137">S_OK</span></span> 
  
> <span data-ttu-id="03923-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="03923-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="03923-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="03923-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="03923-140">MAPI で使用されている SPI バージョンは、このプロバイダーで使用されている SPI と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="03923-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03923-141">注釈</span><span class="sxs-lookup"><span data-stu-id="03923-141">Remarks</span></span>

<span data-ttu-id="03923-142">MAPI は、エントリ ポイント関数 **ABProviderInit** を呼び出して、クライアント ログオン後にアドレス帳プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="03923-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="03923-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="03923-143">Notes to implementers</span></span>

<span data-ttu-id="03923-144">アドレス帳プロバイダーは、プロバイダーの DLL のエントリ ポイント関数として **ABProviderInit** を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03923-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="03923-145">実装は、MAPISPI.H でも指定 **されている ABPROVIDERINIT** 関数プロトタイプに基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="03923-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="03923-146">MAPI では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用する **ABPROVIDERINIT** が定義されています。この場合 **、ABProviderInit** は CDECL 呼び出し規約に従います。</span><span class="sxs-lookup"><span data-stu-id="03923-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="03923-147">同時に複数のプロファイルに表示された結果、または同じプロファイルに複数回表示された結果として、プロバイダーを複数回初期化できます。</span><span class="sxs-lookup"><span data-stu-id="03923-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="03923-148">プロバイダー オブジェクトにはコンテキストが含まれているため **、ABProviderInit** は、同じプロセスで複数の初期化を行う場合でも、初期化ごとに  _lppABProvider_ 内の異なるプロバイダー オブジェクトを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="03923-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="03923-149">アドレス帳プロバイダーは、ほとんどのメモリ割り当てと割り当て解除のために _、lpAllocateBuffer_ _、lpAllocateMore、__および lpFreeBuffer_ が指す関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03923-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="03923-150">特に、 [プロバイダーは、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てるには、これらの関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03923-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="03923-151">プロバイダーが OLE メモリ アロケーターを使用する場合は _、lpMalloc_ パラメーターが指すアロケーター オブジェクトの **IUnknown::AddRef** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="03923-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="03923-152">**ABProviderInit の記述の詳細については、「** アドレス帳プロバイダーエントリ ポイント関数の実装 [」を参照してください](implementing-an-address-book-provider-entry-point-function.md)。</span><span class="sxs-lookup"><span data-stu-id="03923-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="03923-153">エントリ ポイント関数の詳細については、「Service Provider Entry Point Function の実装 [」を参照してください](implementing-a-service-provider-entry-point-function.md)。</span><span class="sxs-lookup"><span data-stu-id="03923-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03923-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="03923-154">See also</span></span>

- [<span data-ttu-id="03923-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03923-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="03923-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="03923-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="03923-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="03923-157">XPProviderInit</span></span>](xpproviderinit.md)

