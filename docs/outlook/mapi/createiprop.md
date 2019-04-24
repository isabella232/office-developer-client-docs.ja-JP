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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333034"
---
# <a name="createiprop"></a><span data-ttu-id="b5676-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="b5676-103">CreateIProp</span></span>

  
  
<span data-ttu-id="b5676-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5676-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5676-105">プロパティデータオブジェクト ( [ipropdata](ipropdataimapiprop.md)オブジェクト) を作成します。</span><span class="sxs-lookup"><span data-stu-id="b5676-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5676-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b5676-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5676-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="b5676-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b5676-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="b5676-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b5676-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b5676-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b5676-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b5676-110">Called by:</span></span>  <br/> |<span data-ttu-id="b5676-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="b5676-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="b5676-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b5676-112">Parameters</span></span>

 <span data-ttu-id="b5676-113">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="b5676-113">_lpInterface_</span></span>
  
> <span data-ttu-id="b5676-114">順番プロパティデータオブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5676-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="b5676-115">有効なインターフェイス識別子は IID_IMAPIPropData です。</span><span class="sxs-lookup"><span data-stu-id="b5676-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="b5676-116">_lpinterface_パラメーターで NULL を渡すと、 _lpppropdata_パラメーターで返される property data オブジェクトが、プロパティデータオブジェクトの標準インターフェイスにキャストされることもあります。</span><span class="sxs-lookup"><span data-stu-id="b5676-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="b5676-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="b5676-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="b5676-118">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5676-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="b5676-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="b5676-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="b5676-120">順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5676-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="b5676-121">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="b5676-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="b5676-122">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5676-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="b5676-123">_lpvreserved_</span><span class="sxs-lookup"><span data-stu-id="b5676-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="b5676-124">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="b5676-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="b5676-125">_lpppropdata_</span><span class="sxs-lookup"><span data-stu-id="b5676-125">_lppPropData_</span></span>
  
> <span data-ttu-id="b5676-126">読み上げ返されたプロパティデータオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b5676-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b5676-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="b5676-127">Return value</span></span>

<span data-ttu-id="b5676-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5676-128">S_OK</span></span> 
  
> <span data-ttu-id="b5676-129">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b5676-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b5676-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b5676-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b5676-131">要求されたインターフェイスは、このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b5676-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5676-132">解説</span><span class="sxs-lookup"><span data-stu-id="b5676-132">Remarks</span></span>

<span data-ttu-id="b5676-133">_lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_の入力パラメーターは、それぞれ、 [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数を指しています。</span><span class="sxs-lookup"><span data-stu-id="b5676-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="b5676-134">**createiprop**を呼び出すクライアントアプリケーションは、という名前の MAPI 関数へのポインターをパスに渡します。サービスプロバイダーは、初期化呼び出しで受け取った、または[imapiallocルーチン](imapisupport-getmemallocroutines.md)メソッドへの呼び出しによって取得したこれらの関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="b5676-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

