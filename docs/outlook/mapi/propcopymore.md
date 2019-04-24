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
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328554"
---
# <a name="propcopymore"></a><span data-ttu-id="58b27-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="58b27-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="58b27-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58b27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58b27-105">1つのプロパティ値をソースの場所から移動先の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="58b27-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58b27-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="58b27-106">Header file:</span></span>  <br/> |<span data-ttu-id="58b27-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="58b27-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="58b27-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="58b27-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="58b27-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="58b27-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="58b27-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="58b27-110">Called by:</span></span>  <br/> |<span data-ttu-id="58b27-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="58b27-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="58b27-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="58b27-112">Parameters</span></span>

 <span data-ttu-id="58b27-113">_lpspropvaluedest_</span><span class="sxs-lookup"><span data-stu-id="58b27-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="58b27-114">読み上げこの関数がコピーされたプロパティ値を定義する[spropvalue](spropvalue.md)構造を書き込む場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="58b27-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="58b27-115">_lpspropて rc_</span><span class="sxs-lookup"><span data-stu-id="58b27-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="58b27-116">順番コピーするプロパティ値を含む[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="58b27-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="58b27-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="58b27-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="58b27-118">順番コピーするプロパティを保持するには、コピー先の場所が十分でない場合に、追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="58b27-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="58b27-119">_lpvobject_</span><span class="sxs-lookup"><span data-stu-id="58b27-119">_lpvObject_</span></span>
  
> <span data-ttu-id="58b27-120">順番**MAPIAllocateMore**が必要に応じてスペースを割り当てるオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="58b27-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="58b27-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="58b27-121">Return value</span></span>

<span data-ttu-id="58b27-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="58b27-122">S_OK</span></span>
  
> <span data-ttu-id="58b27-123">単一のプロパティ値が正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="58b27-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="58b27-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="58b27-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="58b27-125">不明なプロパティの種類が検出されました。</span><span class="sxs-lookup"><span data-stu-id="58b27-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58b27-126">解説</span><span class="sxs-lookup"><span data-stu-id="58b27-126">Remarks</span></span>

<span data-ttu-id="58b27-127">クライアントアプリケーションまたはサービスプロバイダーは、 **propcopymore**関数を使用して、別の場所で使用するために解放されることになるテーブルからプロパティをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="58b27-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="58b27-128">コピーされたプロパティ値が PT_STRING8 など、 [spropvalue](spropvalue.md)構造に適合しない場合を除いて、 **propcopymore**はメモリを割り当てる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="58b27-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="58b27-129">このような大きなプロパティの場合、関数は、ポインターが_lpfAllocMore_パラメータで渡される[MAPIAllocateMore](mapiallocatemore.md)関数を使用してメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="58b27-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="58b27-130">injudicious use **propcopymore**の断片メモリ。代わりに、 [sccopyprops](sccopyprops.md)関数の使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="58b27-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

