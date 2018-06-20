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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 06590fe55cb02b1abf036156877fd308548436f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803864"
---
# <a name="screlocprops"></a><span data-ttu-id="0a34f-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="0a34f-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="0a34f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a34f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a34f-105">[SPropValue](spropvalue.md)配列のポインターは、配列とそのデータがコピーまたは新しい場所に移動された後に調整します。</span><span class="sxs-lookup"><span data-stu-id="0a34f-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a34f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0a34f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a34f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a34f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0a34f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0a34f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0a34f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0a34f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0a34f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0a34f-110">Called by:</span></span>  <br/> |<span data-ttu-id="0a34f-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0a34f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="0a34f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0a34f-112">Parameters</span></span>

 <span data-ttu-id="0a34f-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="0a34f-113">_cprop_</span></span>
  
> <span data-ttu-id="0a34f-114">[in]_Rgprop_パラメーターが指す配列内のプロパティの数です。</span><span class="sxs-lookup"><span data-stu-id="0a34f-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="0a34f-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="0a34f-115">_rgprop_</span></span>
  
> <span data-ttu-id="0a34f-116">[in]ポインターが調整するのには[SPropValue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0a34f-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="0a34f-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="0a34f-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="0a34f-118">[in]_Rgprop_パラメーターが指す配列の元のベース アドレスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="0a34f-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="0a34f-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="0a34f-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="0a34f-120">[in]_Rgprop_パラメーターが指す配列の新しいベース アドレスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="0a34f-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="0a34f-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="0a34f-121">_pcb_</span></span>
  
> <span data-ttu-id="0a34f-122">[で [チェック アウト]ポインターを_pvBaseNew_パラメーターで指定された配列のバイト単位のサイズを指します。</span><span class="sxs-lookup"><span data-stu-id="0a34f-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="0a34f-123">設定されていない場合 NULL の場合、 _pcb_のパラメーターは_pvD_パラメーターに格納されるバイトの数です。</span><span class="sxs-lookup"><span data-stu-id="0a34f-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0a34f-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0a34f-124">Return value</span></span>

<span data-ttu-id="0a34f-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a34f-125">S_OK</span></span>
  
> <span data-ttu-id="0a34f-126">ポインターが正常に調整されました。</span><span class="sxs-lookup"><span data-stu-id="0a34f-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="0a34f-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0a34f-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="0a34f-128">1 つまたは両方のパラメーターが有効でなかったか、不明なプロパティの種類が発生しました。</span><span class="sxs-lookup"><span data-stu-id="0a34f-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a34f-129">備考</span><span class="sxs-lookup"><span data-stu-id="0a34f-129">Remarks</span></span>

<span data-ttu-id="0a34f-130">**ScRelocProps**関数は、ポインターが調整のプロパティ値の配列が最初に割り当てられたの**ScCopyProps**関数の呼び出しのような 1 つの呼び出しであるという前提で動作します。</span><span class="sxs-lookup"><span data-stu-id="0a34f-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="0a34f-131">切り離されたメモリ ブロックから構築されたプロパティの値では、クライアント アプリケーションまたはサービス プロバイダーが動作している場合は、代わりにプロパティをコピーするのには[ScCopyProps](sccopyprops.md)を使用してください。</span><span class="sxs-lookup"><span data-stu-id="0a34f-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="0a34f-132">[SPropValue](spropvalue.md)配列内のポインターの有効性を維持するために**ScRelocProps**が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a34f-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="0a34f-133">ポインターの有効性を保つためにそのような配列を書き込むと、ディスクから読み込むには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="0a34f-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="0a34f-134">アレイとのデータをディスクに書き出す前に、アレイ上のいくつか標準的な値が 0 を指す_pvBaseNew_パラメーターを使用して**ScRelocProps**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0a34f-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="0a34f-135">アレイとのデータをディスクから読み取り後を呼び出す**ScRelocProps** 、 _pvBaseOld_パラメーターを使用してアレイに手順 1 で使用される同じ標準的な値に等しい。</span><span class="sxs-lookup"><span data-stu-id="0a34f-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="0a34f-136">配列およびデータは、1 つの割り当てで作成されたバッファーに読み取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a34f-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="0a34f-137">**ScRelocProps** _pcb_のパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="0a34f-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0a34f-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a34f-138">See also</span></span>



[<span data-ttu-id="0a34f-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0a34f-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="0a34f-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="0a34f-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="0a34f-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="0a34f-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="0a34f-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="0a34f-142">ScRelocNotifications</span></span>](screlocnotifications.md)

