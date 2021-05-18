---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404471"
---
# <a name="propcopymore"></a><span data-ttu-id="cb9d5-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="cb9d5-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="cb9d5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb9d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb9d5-105">1 つのプロパティ値をソースの場所からコピー先の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb9d5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cb9d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="cb9d5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cb9d5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cb9d5-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="cb9d5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cb9d5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cb9d5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cb9d5-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="cb9d5-110">Called by:</span></span>  <br/> |<span data-ttu-id="cb9d5-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cb9d5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="cb9d5-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cb9d5-112">Parameters</span></span>

 <span data-ttu-id="cb9d5-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="cb9d5-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="cb9d5-114">[out]コピーされたプロパティ値を定義する [SPropValue](spropvalue.md) 構造体をこの関数が書き込む場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="cb9d5-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="cb9d5-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="cb9d5-116">[in]コピーする [プロパティ値を含む SPropValue](spropvalue.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="cb9d5-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="cb9d5-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="cb9d5-118">[in]コピー先の場所がコピーするプロパティを保持するのに十分な大きさではない場合に、追加のメモリを割り当てるのに使用する [MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="cb9d5-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="cb9d5-119">_lpvObject_</span></span>
  
> <span data-ttu-id="cb9d5-120">[in] **MAPIAllocateMore** が必要に応じて領域を割り当てるオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cb9d5-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="cb9d5-121">Return value</span></span>

<span data-ttu-id="cb9d5-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb9d5-122">S_OK</span></span>
  
> <span data-ttu-id="cb9d5-123">単一のプロパティ値が正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="cb9d5-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cb9d5-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="cb9d5-125">不明なプロパティの種類が検出されました。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb9d5-126">注釈</span><span class="sxs-lookup"><span data-stu-id="cb9d5-126">Remarks</span></span>

<span data-ttu-id="cb9d5-127">クライアント アプリケーションまたはサービス プロバイダーは **PropCopyMore** 関数を使用して、他の場所でプロパティを使用するために解放されるテーブルからプロパティをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="cb9d5-128">**PropCopyMore は** 、コピーされるプロパティ値が [sPropValue](spropvalue.md) 構造体に収まらない PT_STRING8 などの型の場合を指定しない限り、メモリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="cb9d5-129">これらの大きなプロパティの場合、関数は、ポインターが _lpfAllocMore_ パラメーターで渡される [MAPIAllocateMore](mapiallocatemore.md)関数を使用してメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="cb9d5-130">**PropCopyMore** フラグメント メモリの不当な使用。代わりに [ScCopyProps 関数の使用](sccopyprops.md)を検討してください。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

