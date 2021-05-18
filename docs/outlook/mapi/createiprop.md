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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406809"
---
# <a name="createiprop"></a><span data-ttu-id="636a7-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="636a7-103">CreateIProp</span></span>

  
  
<span data-ttu-id="636a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="636a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="636a7-105">プロパティ データ オブジェクト (つまり [、IPropData](ipropdataimapiprop.md) オブジェクト) を作成します。</span><span class="sxs-lookup"><span data-stu-id="636a7-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="636a7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="636a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="636a7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="636a7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="636a7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="636a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="636a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="636a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="636a7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="636a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="636a7-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="636a7-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="636a7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="636a7-112">Parameters</span></span>

 <span data-ttu-id="636a7-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="636a7-113">_lpInterface_</span></span>
  
> <span data-ttu-id="636a7-114">[in]プロパティ データ オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="636a7-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="636a7-115">有効なインターフェイス識別子はIID_IMAPIPropData。</span><span class="sxs-lookup"><span data-stu-id="636a7-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="636a7-116">_lpInterface_ パラメーターに NULL を渡した場合 _、lppPropData_ パラメーターで返されるプロパティ データ オブジェクトも、プロパティ データ オブジェクトの標準インターフェイスにキャストされます。</span><span class="sxs-lookup"><span data-stu-id="636a7-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="636a7-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="636a7-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="636a7-118">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="636a7-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="636a7-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="636a7-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="636a7-120">[in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="636a7-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="636a7-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="636a7-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="636a7-122">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="636a7-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="636a7-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="636a7-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="636a7-124">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="636a7-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="636a7-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="636a7-125">_lppPropData_</span></span>
  
> <span data-ttu-id="636a7-126">[out]返されるプロパティ データ オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="636a7-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="636a7-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="636a7-127">Return value</span></span>

<span data-ttu-id="636a7-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="636a7-128">S_OK</span></span> 
  
> <span data-ttu-id="636a7-129">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="636a7-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="636a7-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="636a7-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="636a7-131">要求されたインターフェイスは、このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="636a7-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="636a7-132">注釈</span><span class="sxs-lookup"><span data-stu-id="636a7-132">Remarks</span></span>

<span data-ttu-id="636a7-133">_lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ 入力パラメーターは [、MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer](mapiallocatebuffer.md)関数をそれぞれ指します。  [](mapiallocatemore.md) [](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="636a7-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="636a7-134">**CreateIProp を呼び出すクライアント** アプリケーションは、という名前の MAPI 関数へのポインターを渡します。サービス プロバイダーは、初期化呼び出しで受信した、[または IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドへの呼び出しで取得されたこれらの関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="636a7-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

