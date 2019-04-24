---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360691"
---
# <a name="screlocprops"></a><span data-ttu-id="9b893-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="9b893-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="9b893-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b893-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b893-105">配列とそのデータが新しい場所にコピーまたは移動された後に、 [spropvalue](spropvalue.md)配列内のポインターを調整します。</span><span class="sxs-lookup"><span data-stu-id="9b893-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b893-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9b893-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b893-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b893-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9b893-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="9b893-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9b893-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9b893-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9b893-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="9b893-110">Called by:</span></span>  <br/> |<span data-ttu-id="9b893-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="9b893-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="9b893-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b893-112">Parameters</span></span>

 <span data-ttu-id="9b893-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="9b893-113">_cprop_</span></span>
  
> <span data-ttu-id="9b893-114">順番_rgprop_パラメーターによって参照される、配列内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="9b893-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="9b893-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="9b893-115">_rgprop_</span></span>
  
> <span data-ttu-id="9b893-116">順番ポインターを調整する[spropvalue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b893-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="9b893-117">_pvbaseold_</span><span class="sxs-lookup"><span data-stu-id="9b893-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="9b893-118">順番_rgprop_パラメーターによって参照される配列の元のベースアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b893-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="9b893-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="9b893-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="9b893-120">順番_rgprop_パラメーターによって参照される配列の新しいベースアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b893-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="9b893-121">_設計_</span><span class="sxs-lookup"><span data-stu-id="9b893-121">_pcb_</span></span>
  
> <span data-ttu-id="9b893-122">[入力]_pvBaseNew_パラメーターで指定された配列のサイズをバイト単位で示すオプションのポインターです。</span><span class="sxs-lookup"><span data-stu-id="9b893-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="9b893-123">NULL でない場合、 _pcb_パラメーターは_pvD_パラメータに格納されているバイト数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9b893-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9b893-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="9b893-124">Return value</span></span>

<span data-ttu-id="9b893-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b893-125">S_OK</span></span>
  
> <span data-ttu-id="9b893-126">ポインターが正常に調整されました。</span><span class="sxs-lookup"><span data-stu-id="9b893-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="9b893-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9b893-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="9b893-128">1つまたは両方のパラメーターが無効であったか、不明なプロパティの種類が検出されました。</span><span class="sxs-lookup"><span data-stu-id="9b893-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b893-129">解説</span><span class="sxs-lookup"><span data-stu-id="9b893-129">Remarks</span></span>

<span data-ttu-id="9b893-130">**ScRelocProps**関数は、ポインターが調整されているプロパティ値の配列が、 **sccopyprops**関数の呼び出しと同じように、1つの呼び出しで最初に割り当てられたことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="9b893-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="9b893-131">クライアントアプリケーションまたはサービスプロバイダーが、メモリのないブロックから構築されたプロパティ値を処理している場合は、 [sccopyprops](sccopyprops.md)を使用してプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b893-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="9b893-132">**ScRelocProps**は、 [spropvalue](spropvalue.md)配列内のポインターの有効性を維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b893-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="9b893-133">このような配列を書き込み、ディスクから読み取る際にポインターの有効性を維持するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9b893-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="9b893-134">配列とデータをディスクに書き込む前に、 _pvBaseNew_パラメーターを指定した配列の**ScRelocProps**を、たとえば、何らかの標準値ゼロを指定して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b893-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="9b893-135">ディスクから配列とデータを読み取った後、手順1で使用したのと同じ標準値に等しい_pvbaseold_パラメーターを持つ配列で**ScRelocProps**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b893-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="9b893-136">配列とデータは、1つの割り当てで作成されたバッファーに読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b893-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="9b893-137">**ScRelocProps**の_pcb_パラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="9b893-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9b893-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b893-138">See also</span></span>



[<span data-ttu-id="9b893-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9b893-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9b893-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="9b893-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="9b893-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="9b893-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="9b893-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="9b893-142">ScRelocNotifications</span></span>](screlocnotifications.md)

