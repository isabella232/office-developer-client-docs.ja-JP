---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 906dc4a24b994e079a977808c3f501aaaea9d84f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799859"
---
# <a name="createiprop"></a><span data-ttu-id="c49e0-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="c49e0-103">CreateIProp</span></span>

  
  
<span data-ttu-id="c49e0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c49e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c49e0-105">プロパティのデータ オブジェクトは、 [IPropData](ipropdataimapiprop.md)オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c49e0-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c49e0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c49e0-106">Header file:</span></span>  <br/> |<span data-ttu-id="c49e0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c49e0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c49e0-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c49e0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c49e0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c49e0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c49e0-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c49e0-110">Called by:</span></span>  <br/> |<span data-ttu-id="c49e0-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c49e0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a><span data-ttu-id="c49e0-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="c49e0-112">Parameters</span></span>

 <span data-ttu-id="c49e0-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c49e0-113">_lpInterface_</span></span>
  
> <span data-ttu-id="c49e0-114">[in]インターフェイス識別子 (IID) のプロパティのデータ オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49e0-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="c49e0-115">有効なインタ フェース識別子は、IID_IMAPIPropData です。</span><span class="sxs-lookup"><span data-stu-id="c49e0-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="c49e0-116">プロパティのデータ オブジェクトの標準的なインターフェイスにキャストするのには_lppPropData_パラメーターで返されるプロパティのデータ オブジェクトは、 _lpInterface_パラメーターに NULL を渡すことも。</span><span class="sxs-lookup"><span data-stu-id="c49e0-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="c49e0-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="c49e0-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="c49e0-118">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49e0-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="c49e0-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="c49e0-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="c49e0-120">[in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49e0-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="c49e0-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="c49e0-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="c49e0-122">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49e0-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="c49e0-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="c49e0-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="c49e0-124">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c49e0-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="c49e0-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="c49e0-125">_lppPropData_</span></span>
  
> <span data-ttu-id="c49e0-126">[out]返されるプロパティのデータ オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c49e0-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c49e0-127">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c49e0-127">Return value</span></span>

<span data-ttu-id="c49e0-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="c49e0-128">S_OK</span></span> 
  
> <span data-ttu-id="c49e0-129">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c49e0-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c49e0-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="c49e0-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="c49e0-131">このオブジェクトには、要求されたインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c49e0-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c49e0-132">備考</span><span class="sxs-lookup"><span data-stu-id="c49e0-132">Remarks</span></span>

<span data-ttu-id="c49e0-133">_LpAllocateBuffer_、 _lpAllocateMore_、および_lpFreeBuffer_の入力パラメーターは、それぞれ[MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数では、] をポイントします。</span><span class="sxs-lookup"><span data-stu-id="c49e0-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="c49e0-134">**CreateIProp**を呼び出すクライアント アプリケーションが MAPI の関数を同じ名前でポインターを渡しますサービス プロバイダーは、これらの関数は、初期化の呼び出しで受信した、 [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドの呼び出しで取得したポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="c49e0-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

