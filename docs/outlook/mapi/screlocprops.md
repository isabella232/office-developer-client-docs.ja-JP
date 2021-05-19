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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421089"
---
# <a name="screlocprops"></a><span data-ttu-id="058fd-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="058fd-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="058fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="058fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="058fd-105">配列とそのデータがコピーまたは新しい場所に移動された後 [、SPropValue](spropvalue.md) 配列内のポインターを調整します。</span><span class="sxs-lookup"><span data-stu-id="058fd-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="058fd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="058fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="058fd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="058fd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="058fd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="058fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="058fd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="058fd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="058fd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="058fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="058fd-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="058fd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="058fd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="058fd-112">Parameters</span></span>

 <span data-ttu-id="058fd-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="058fd-113">_cprop_</span></span>
  
> <span data-ttu-id="058fd-114">[in]  _rgprop_ パラメーターが指す配列内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="058fd-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="058fd-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="058fd-115">_rgprop_</span></span>
  
> <span data-ttu-id="058fd-116">[in]ポインターを調整する [SPropValue](spropvalue.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="058fd-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="058fd-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="058fd-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="058fd-118">[in]  _rgprop_ パラメーターが指す配列の元のベース アドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="058fd-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="058fd-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="058fd-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="058fd-120">[in]  _rgprop_ パラメーターが指す配列の新しいベース アドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="058fd-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="058fd-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="058fd-121">_pcb_</span></span>
  
> <span data-ttu-id="058fd-122">[in, out]  _pvBaseNew_ パラメーターで示される配列のサイズ (バイト単位) へのオプションのポインター。</span><span class="sxs-lookup"><span data-stu-id="058fd-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="058fd-123">NULL 以外の場合  _、pcb_ パラメーターは pvD パラメーターに格納されているバイト数  _に設定_ されます。</span><span class="sxs-lookup"><span data-stu-id="058fd-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="058fd-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="058fd-124">Return value</span></span>

<span data-ttu-id="058fd-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="058fd-125">S_OK</span></span>
  
> <span data-ttu-id="058fd-126">ポインターが正常に調整されました。</span><span class="sxs-lookup"><span data-stu-id="058fd-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="058fd-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="058fd-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="058fd-128">1 つまたは両方のパラメーターが無効であるか、不明なプロパティの種類が検出されました。</span><span class="sxs-lookup"><span data-stu-id="058fd-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="058fd-129">注釈</span><span class="sxs-lookup"><span data-stu-id="058fd-129">Remarks</span></span>

<span data-ttu-id="058fd-130">**ScRelocProps** 関数は、ポインターが調整されるプロパティ値配列が **、ScCopyProps** 関数の呼び出しと同様の 1 回の呼び出しで最初に割り当てられたという前提で動作します。</span><span class="sxs-lookup"><span data-stu-id="058fd-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="058fd-131">クライアント アプリケーションまたはサービス プロバイダーが、バラバラのメモリ ブロックから構築されたプロパティ値を使用している場合は [、ScCopyProps](sccopyprops.md) を使用して代わりにプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="058fd-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="058fd-132">**ScRelocProps は**[、SPropValue](spropvalue.md)配列内のポインターの有効性を維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="058fd-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="058fd-133">このような配列をディスクに書き込んでディスクから読み取る際にポインターの有効性を維持するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="058fd-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="058fd-134">配列とデータをディスクに書き込む前に、_たとえば、標準_ 値 0 を指す pvBaseNew パラメーターを使用して、配列の **ScRelocProps** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="058fd-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="058fd-135">ディスクから配列とデータを読み取った後、手順 1 で使用した標準値と同じ pvBaseOld パラメーターを使用して、配列の **ScRelocProps** を呼び出します。 </span><span class="sxs-lookup"><span data-stu-id="058fd-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="058fd-136">配列とデータは、1 つの割り当てで作成されたバッファーに読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="058fd-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="058fd-137">**ScRelocProps への pcb パラメーターは** オプションです。 </span><span class="sxs-lookup"><span data-stu-id="058fd-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="058fd-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="058fd-138">See also</span></span>



[<span data-ttu-id="058fd-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="058fd-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="058fd-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="058fd-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="058fd-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="058fd-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="058fd-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="058fd-142">ScRelocNotifications</span></span>](screlocnotifications.md)

