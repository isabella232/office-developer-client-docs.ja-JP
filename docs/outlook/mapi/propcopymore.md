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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 750d8b8d50acb9cf7340e6553062412667398665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803693"
---
# <a name="propcopymore"></a><span data-ttu-id="49603-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="49603-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="49603-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49603-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49603-105">1 つのプロパティの値を元の場所から先の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="49603-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49603-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="49603-106">Header file:</span></span>  <br/> |<span data-ttu-id="49603-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="49603-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="49603-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="49603-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="49603-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="49603-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="49603-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="49603-110">Called by:</span></span>  <br/> |<span data-ttu-id="49603-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="49603-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="49603-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49603-112">Parameters</span></span>

 <span data-ttu-id="49603-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="49603-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="49603-114">[out]書き込みます、 [SPropValue](spropvalue.md)構造体がコピーされたプロパティ値を定義する場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="49603-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="49603-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="49603-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="49603-116">[in]コピーするプロパティの値を含む[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="49603-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="49603-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="49603-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="49603-118">[in]先にコピーするプロパティを保持するのに十分な大きさがない場合、追加のメモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="49603-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="49603-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="49603-119">_lpvObject_</span></span>
  
> <span data-ttu-id="49603-120">[in]対象の**MAPIAllocateMore**は領域を割り当てる必要がある場合、オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="49603-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="49603-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="49603-121">Return value</span></span>

<span data-ttu-id="49603-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="49603-122">S_OK</span></span>
  
> <span data-ttu-id="49603-123">1 つのプロパティの値は、正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="49603-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="49603-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="49603-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="49603-125">不明なプロパティの種類が発生しました。</span><span class="sxs-lookup"><span data-stu-id="49603-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49603-126">注釈</span><span class="sxs-lookup"><span data-stu-id="49603-126">Remarks</span></span>

<span data-ttu-id="49603-127">クライアント アプリケーションまたはサービス プロバイダーは、それを別の場所で使用するために解放しようとしているテーブルのプロパティをコピーするのには、 **PropCopyMore**関数を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="49603-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="49603-128">**PropCopyMore**は PT_STRING8、 [SPropValue](spropvalue.md)構造に適合しないなどの型がプロパティの値をコピーしない限り、メモリを割り当てる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="49603-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="49603-129">、これらの大規模なプロパティは、関数は、 _lpfAllocMore_パラメーターで、ポインターが渡されます[MAPIAllocateMore](mapiallocatemore.md)関数を使用してメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="49603-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="49603-130">**PropCopyMore**の injudicious の使用にはメモリがフラグメント化します。代わりに[ScCopyProps](sccopyprops.md)関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="49603-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

