---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eb3b3b3c9c2e9cffb77febf9c96baed40ce3f9e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566223"
---
# <a name="sccopyprops"></a><span data-ttu-id="40424-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="40424-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="40424-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40424-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40424-105">コピーのプロパティは、新しいターゲットに[SPropValue](spropvalue.md)構造体の配列によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="40424-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40424-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="40424-106">Header file:</span></span>  <br/> |<span data-ttu-id="40424-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="40424-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="40424-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="40424-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="40424-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="40424-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="40424-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="40424-110">Called by:</span></span>  <br/> |<span data-ttu-id="40424-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="40424-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="40424-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="40424-112">Parameters</span></span>

 <span data-ttu-id="40424-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="40424-113">_cprop_</span></span>
  
> <span data-ttu-id="40424-114">[in]コピーするプロパティの数です。</span><span class="sxs-lookup"><span data-stu-id="40424-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="40424-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="40424-115">_rgprop_</span></span>
  
> <span data-ttu-id="40424-116">[in]コピーするプロパティを定義する[SPropValue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40424-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="40424-117">_Rgprop_パラメーターを配列の先頭をポイントする必要はありませんが、 **SPropValue**構造体、配列内のいずれかの先頭を指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="40424-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="40424-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="40424-118">_pvDst_</span></span>
  
> <span data-ttu-id="40424-119">[in]この関数のプロパティをコピーする先のメモリ内の最初の位置へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40424-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="40424-120">_pcb_</span><span class="sxs-lookup"><span data-stu-id="40424-120">_pcb_</span></span>
  
> <span data-ttu-id="40424-121">[out]ポインターを_pvDst_パラメーターが指すメモリ ブロックのバイト単位のサイズを指します。</span><span class="sxs-lookup"><span data-stu-id="40424-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="40424-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="40424-122">Return value</span></span>

<span data-ttu-id="40424-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="40424-123">S_OK</span></span>
  
> <span data-ttu-id="40424-124">プロパティが正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="40424-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="40424-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40424-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="40424-126">不明なプロパティの種類が発生しました。</span><span class="sxs-lookup"><span data-stu-id="40424-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40424-127">注釈</span><span class="sxs-lookup"><span data-stu-id="40424-127">Remarks</span></span>

<span data-ttu-id="40424-128">新しい配列とそのデータは、1 つの割り当てで作成されたバッファー内に存在し、個別の[SPropValue](spropvalue.md)構造体のポインターを調整する[ScRelocProps](screlocprops.md)関数を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="40424-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="40424-129">この調整をする前に、ポインターは有効です。</span><span class="sxs-lookup"><span data-stu-id="40424-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="40424-130">**ScCopyProps**は、コピーされたプロパティの配列を元のプロパティの順序を維持します。</span><span class="sxs-lookup"><span data-stu-id="40424-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="40424-131">_Pcb_のパラメーターは省略可能です。それが NULL でない場合は、 _pvDst_パラメーターに格納されているバイト数に設定されています。</span><span class="sxs-lookup"><span data-stu-id="40424-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40424-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="40424-132">See also</span></span>



[<span data-ttu-id="40424-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="40424-133">ScDupPropset</span></span>](scduppropset.md)

