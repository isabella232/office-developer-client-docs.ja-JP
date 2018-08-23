---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583352"
---
# <a name="sccountprops"></a><span data-ttu-id="60ad3-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="60ad3-103">ScCountProps</span></span>

  
  
<span data-ttu-id="60ad3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60ad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60ad3-105">プロパティ値の配列のバイト単位のサイズを決定し、配列に関連付けられているメモリを確認します。</span><span class="sxs-lookup"><span data-stu-id="60ad3-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60ad3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="60ad3-106">Header file:</span></span>  <br/> |<span data-ttu-id="60ad3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="60ad3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="60ad3-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="60ad3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="60ad3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="60ad3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="60ad3-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="60ad3-110">Called by:</span></span>  <br/> |<span data-ttu-id="60ad3-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="60ad3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="60ad3-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="60ad3-112">Parameters</span></span>

 <span data-ttu-id="60ad3-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="60ad3-113">_cprop_</span></span>
  
> <span data-ttu-id="60ad3-114">[in]_Rgprop_パラメーターで指定された配列内のプロパティの数です。</span><span class="sxs-lookup"><span data-stu-id="60ad3-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="60ad3-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="60ad3-115">_rgprop_</span></span>
  
> <span data-ttu-id="60ad3-116">[in][SPropValue](spropvalue.md)構造体のサイズを確認するプロパティを定義する配列内の範囲へのポインター。</span><span class="sxs-lookup"><span data-stu-id="60ad3-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="60ad3-117">この範囲は、配列の先頭に必ずしも起動しません。</span><span class="sxs-lookup"><span data-stu-id="60ad3-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="60ad3-118">_pcb_</span><span class="sxs-lookup"><span data-stu-id="60ad3-118">_pcb_</span></span>
  
> <span data-ttu-id="60ad3-119">[out]ポインターをプロパティの配列のバイト単位のサイズを指します。</span><span class="sxs-lookup"><span data-stu-id="60ad3-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60ad3-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="60ad3-120">Return value</span></span>

<span data-ttu-id="60ad3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="60ad3-121">S_OK</span></span> 
  
> <span data-ttu-id="60ad3-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="60ad3-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="60ad3-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="60ad3-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="60ad3-124">PROP_ID_NULL または PROP_ID_INVALID の識別子のプロパティ値の配列内の少なくとも 1 つのプロパティまたはプロパティ配列には、複数値を持つプロパティ値のないプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="60ad3-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60ad3-125">注釈</span><span class="sxs-lookup"><span data-stu-id="60ad3-125">Remarks</span></span>

<span data-ttu-id="60ad3-126">_Pcb_のパラメーターに NULL が渡されると、通知の配列を検証する**ScCountProps**関数が、カウントは行われません。</span><span class="sxs-lookup"><span data-stu-id="60ad3-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="60ad3-127">**ScCountNotifications**関数が配列のサイズを決定し、原因を格納する_pcb_の null 以外の値が渡された場合_pcb_です。</span><span class="sxs-lookup"><span data-stu-id="60ad3-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="60ad3-128">_Pcb_のパラメーターは、配列全体を格納できる大きさである必要があります。</span><span class="sxs-lookup"><span data-stu-id="60ad3-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="60ad3-129">それがカウントと**ScCountProps**は、配列に関連付けられているメモリを検証します。</span><span class="sxs-lookup"><span data-stu-id="60ad3-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="60ad3-130">**ScCountProps**は、MAPI に関する情報を持つプロパティでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="60ad3-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60ad3-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="60ad3-131">See also</span></span>



[<span data-ttu-id="60ad3-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="60ad3-132">PropCopyMore</span></span>](propcopymore.md)

