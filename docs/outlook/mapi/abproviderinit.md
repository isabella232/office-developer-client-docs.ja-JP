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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799613"
---
# <a name="abproviderinit"></a><span data-ttu-id="0aed2-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="0aed2-103">ABProviderInit</span></span>
 
<span data-ttu-id="0aed2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0aed2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0aed2-105">操作のためのアドレス帳プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0aed2-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0aed2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0aed2-106">Header file:</span></span>  <br/> |<span data-ttu-id="0aed2-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="0aed2-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="0aed2-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0aed2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0aed2-109">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0aed2-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="0aed2-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0aed2-110">Called by:</span></span>  <br/> |<span data-ttu-id="0aed2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0aed2-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0aed2-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0aed2-112">Parameters</span></span>

 <span data-ttu-id="0aed2-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="0aed2-113">_hInstance_</span></span>
  
> <span data-ttu-id="0aed2-114">[in]それにリンクされている場合に使用される MAPI アドレス帳プロバイダーのダイナミック リンク ライブラリ (DLL) のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="0aed2-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="0aed2-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="0aed2-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="0aed2-116">[in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0aed2-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="0aed2-117">アドレス帳プロバイダーは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aed2-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="0aed2-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="0aed2-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="0aed2-119">[in]使用して MAPI によって必要なメモリを割り当て、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0aed2-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="0aed2-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="0aed2-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="0aed2-121">[in]使用して MAPI によって必要に応じて追加のメモリを割り当て、 [MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0aed2-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="0aed2-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="0aed2-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="0aed2-123">[in]MAPI によってメモリを解放するために必要な場合に使用する[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0aed2-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="0aed2-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0aed2-124">_ulFlags_</span></span>
  
> <span data-ttu-id="0aed2-125">[in]フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="0aed2-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="0aed2-126">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0aed2-126">The following flag can be set:</span></span>
    
<span data-ttu-id="0aed2-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="0aed2-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="0aed2-128">プロバイダーは、Windows サービス、特別な種類のすべてのユーザー インターフェイスにアクセスすることがなくプロセスのコンテキストで行われます。</span><span class="sxs-lookup"><span data-stu-id="0aed2-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="0aed2-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="0aed2-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="0aed2-130">[in]サービス プロバイダー インターフェイス (SPI)、MAPI のバージョン番号です。DLL を使用します。</span><span class="sxs-lookup"><span data-stu-id="0aed2-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="0aed2-131">現在のバージョン番号は、MAPISPI を参照してください。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="0aed2-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="0aed2-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="0aed2-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="0aed2-133">[out]このアドレス帳プロバイダーを使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0aed2-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="0aed2-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="0aed2-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="0aed2-135">[out]初期化済みのアドレス帳プロバイダー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0aed2-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0aed2-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0aed2-136">Return value</span></span>

<span data-ttu-id="0aed2-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="0aed2-137">S_OK</span></span> 
  
> <span data-ttu-id="0aed2-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0aed2-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0aed2-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="0aed2-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="0aed2-140">MAPI によって使用されている SPI のバージョンは、このプロバイダーで使用されている SPI との互換性ではありません。</span><span class="sxs-lookup"><span data-stu-id="0aed2-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aed2-141">注釈</span><span class="sxs-lookup"><span data-stu-id="0aed2-141">Remarks</span></span>

<span data-ttu-id="0aed2-142">MAPI は、クライアント ログオンの後、アドレス帳プロバイダーを初期化するために**ABProviderInit**エントリ ポイント関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0aed2-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0aed2-143">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="0aed2-143">Notes to implementers</span></span>

<span data-ttu-id="0aed2-144">アドレス帳プロバイダーは、プロバイダーの DLL にエントリ ポイント関数として**ABProviderInit**を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aed2-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="0aed2-145">実装は、 **ABPROVIDERINIT**関数のプロトタイプで指定されている MAPISPI もに基づいている必要があります。H.</span><span class="sxs-lookup"><span data-stu-id="0aed2-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="0aed2-146">MAPI では、型を使用する標準的な MAPI の初期化の呼び出し、CDECL 呼び出し規約に従う**ABProviderInit**を STDMAPIINITCALLTYPE、 **ABPROVIDERINIT**を定義します。</span><span class="sxs-lookup"><span data-stu-id="0aed2-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="0aed2-147">プロバイダーは、同時使用中、または同じプロファイルで複数回表示されるは、いくつかのプロファイルに表示されるため、複数回初期化できます。</span><span class="sxs-lookup"><span data-stu-id="0aed2-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="0aed2-148">プロバイダー オブジェクトには、コンテキストが含まれている、ため**ABProviderInit**ごとの初期化を同じプロセスで複数回初期化の場合でも_lppABProvider_で、別のプロバイダー オブジェクトを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aed2-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="0aed2-149">アドレス帳プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと割り当て解除の_lpFreeBuffer_が指す関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aed2-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="0aed2-150">具体的には、プロバイダーでは、 [IMAPIProp::GetProps](imapiprop-getprops.md)や[IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当てにこれらの関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aed2-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="0aed2-151">プロバイダーは、OLE のメモリ アロケーターを使用しても期待しています、する場合は、 _lpMalloc_パラメーターで指定されたアロケーター オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0aed2-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="0aed2-152">**ABProviderInit**の作成方法の詳細については、[アドレス帳プロバイダーのエントリ ポイント関数を実装する](implementing-an-address-book-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aed2-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="0aed2-153">エントリ ポイント関数の詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aed2-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0aed2-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="0aed2-154">See also</span></span>

- [<span data-ttu-id="0aed2-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0aed2-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="0aed2-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="0aed2-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="0aed2-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="0aed2-157">XPProviderInit</span></span>](xpproviderinit.md)

