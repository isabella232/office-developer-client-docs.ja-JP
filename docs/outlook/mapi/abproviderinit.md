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
# <a name="abproviderinit"></a><span data-ttu-id="a25cb-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="a25cb-103">ABProviderInit</span></span>
 
<span data-ttu-id="a25cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a25cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a25cb-105">操作のアドレス帳プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a25cb-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a25cb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a25cb-106">Header file:</span></span>  <br/> |<span data-ttu-id="a25cb-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="a25cb-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a25cb-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a25cb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a25cb-109">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a25cb-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="a25cb-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a25cb-110">Called by:</span></span>  <br/> |<span data-ttu-id="a25cb-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a25cb-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a25cb-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a25cb-112">Parameters</span></span>

 <span data-ttu-id="a25cb-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="a25cb-113">_hInstance_</span></span>
  
> <span data-ttu-id="a25cb-114">順番MAPI がリンクしたときに使用したアドレス帳プロバイダーのダイナミックリンクライブラリ (DLL) のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="a25cb-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="a25cb-115">_lpmalloc_</span><span class="sxs-lookup"><span data-stu-id="a25cb-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="a25cb-116">順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a25cb-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="a25cb-117">**IStream**など特定のインターフェイスを使用している場合、アドレス帳プロバイダーはこの割り当て方法を使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="a25cb-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="a25cb-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="a25cb-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="a25cb-119">順番MAPI がメモリを割り当てる際に必要となる、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a25cb-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="a25cb-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="a25cb-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="a25cb-121">順番MAPI が追加のメモリを割り当てる際に必要な、 [MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a25cb-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="a25cb-122">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="a25cb-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="a25cb-123">順番MAPI がメモリを解放するために必要な場合に使用される、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a25cb-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="a25cb-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a25cb-124">_ulFlags_</span></span>
  
> <span data-ttu-id="a25cb-125">順番フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a25cb-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="a25cb-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a25cb-126">The following flag can be set:</span></span>
    
<span data-ttu-id="a25cb-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="a25cb-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="a25cb-128">プロバイダーは、ユーザーインターフェイスにアクセスできない特別な種類のプロセスである Windows サービスのコンテキストに読み込まれています。</span><span class="sxs-lookup"><span data-stu-id="a25cb-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="a25cb-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="a25cb-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="a25cb-130">順番MAPI が提供するサービスプロバイダインターフェイス (SPI) のバージョン番号。DLL はを使用します。</span><span class="sxs-lookup"><span data-stu-id="a25cb-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="a25cb-131">現在のバージョン番号については、MAPISPI を参照してください。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="a25cb-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="a25cb-132">_lアウト providerver_</span><span class="sxs-lookup"><span data-stu-id="a25cb-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="a25cb-133">読み上げこのアドレス帳プロバイダーが使用する SPI のバージョン番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a25cb-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="a25cb-134">_lppabprovider_</span><span class="sxs-lookup"><span data-stu-id="a25cb-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="a25cb-135">読み上げ初期化されたアドレス帳プロバイダオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a25cb-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a25cb-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="a25cb-136">Return value</span></span>

<span data-ttu-id="a25cb-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="a25cb-137">S_OK</span></span> 
  
> <span data-ttu-id="a25cb-138">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a25cb-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a25cb-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="a25cb-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="a25cb-140">MAPI で使用されている spi バージョンは、このプロバイダーで使用されている spi と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="a25cb-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a25cb-141">注釈</span><span class="sxs-lookup"><span data-stu-id="a25cb-141">Remarks</span></span>

<span data-ttu-id="a25cb-142">MAPI はエントリポイント関数**abproviderinit**を呼び出して、クライアントログオンの後にアドレス帳プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a25cb-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a25cb-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="a25cb-143">Notes to implementers</span></span>

<span data-ttu-id="a25cb-144">アドレス帳プロバイダーは、 **abproviderinit**をプロバイダーの DLL のエントリポイント関数として実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a25cb-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="a25cb-145">この実装は、MAPISPI でも指定されている**abproviderinit**関数プロトタイプに基づいている必要があります。H.</span><span class="sxs-lookup"><span data-stu-id="a25cb-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="a25cb-146">mapi では、標準の MAPI 初期化呼び出しの種類 STDMAPIINITCALLTYPE を使用するように**abproviderinit**が定義されており、これにより、 **abproviderinit**が CDECL 呼び出し規則に従います。</span><span class="sxs-lookup"><span data-stu-id="a25cb-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="a25cb-147">プロバイダーは、複数のプロファイルに同時に使用された結果、または同じプロファイルに複数回出現した結果として、複数回初期化することができます。</span><span class="sxs-lookup"><span data-stu-id="a25cb-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="a25cb-148">プロバイダーオブジェクトにはコンテキストが含まれているため、同じプロセス内で複数の初期化があっても、 **abproviderinit**がそれぞれの異なるプロバイダーオブジェクトを_lppabprovider_で返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a25cb-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="a25cb-149">アドレス帳プロバイダーは、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、ほとんどのメモリの割り当てと割り当てを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a25cb-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="a25cb-150">特に、プロバイダーはこれらの関数を使用して、 [imapiprop:: GetProps](imapiprop-getprops.md) 、 [IMAPITable:: QueryRows](imapitable-queryrows.md)などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a25cb-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="a25cb-151">プロバイダーが OLE メモリアロケーターを使用することを前提としている場合は、 _lpmalloc_パラメーターで指定されたアロケーターオブジェクトの**IUnknown:: AddRef**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a25cb-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="a25cb-152">**abproviderinit**の記述の詳細については、「[アドレス帳プロバイダーエントリポイント関数の実装](implementing-an-address-book-provider-entry-point-function.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a25cb-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="a25cb-153">エントリポイント関数の詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a25cb-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a25cb-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="a25cb-154">See also</span></span>

- [<span data-ttu-id="a25cb-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a25cb-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="a25cb-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="a25cb-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="a25cb-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="a25cb-157">XPProviderInit</span></span>](xpproviderinit.md)

