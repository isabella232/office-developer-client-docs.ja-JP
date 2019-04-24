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
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351318"
---
# <a name="sccountprops"></a><span data-ttu-id="3912d-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="3912d-103">ScCountProps</span></span>

  
  
<span data-ttu-id="3912d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3912d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3912d-105">プロパティ値の配列のサイズをバイト単位で指定し、配列に関連付けられているメモリを検証します。</span><span class="sxs-lookup"><span data-stu-id="3912d-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3912d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3912d-106">Header file:</span></span>  <br/> |<span data-ttu-id="3912d-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="3912d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3912d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="3912d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3912d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3912d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3912d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3912d-110">Called by:</span></span>  <br/> |<span data-ttu-id="3912d-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="3912d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="3912d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3912d-112">Parameters</span></span>

 <span data-ttu-id="3912d-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="3912d-113">_cprop_</span></span>
  
> <span data-ttu-id="3912d-114">順番_rgprop_パラメーターによって示される、配列内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="3912d-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="3912d-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="3912d-115">_rgprop_</span></span>
  
> <span data-ttu-id="3912d-116">順番サイズを決定するプロパティを定義する[spropvalue](spropvalue.md)構造体の配列内の範囲へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3912d-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="3912d-117">この範囲は、必ずしも配列の先頭から開始することはできません。</span><span class="sxs-lookup"><span data-stu-id="3912d-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="3912d-118">_設計_</span><span class="sxs-lookup"><span data-stu-id="3912d-118">_pcb_</span></span>
  
> <span data-ttu-id="3912d-119">読み上げ(オプション) プロパティ配列のサイズ (バイト単位) のポインターです。</span><span class="sxs-lookup"><span data-stu-id="3912d-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3912d-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="3912d-120">Return value</span></span>

<span data-ttu-id="3912d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3912d-121">S_OK</span></span> 
  
> <span data-ttu-id="3912d-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3912d-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3912d-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3912d-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="3912d-124">プロパティ値配列の少なくとも1つのプロパティに PROP_ID_NULL または PROP_ID_INVALID の識別子があるか、プロパティ配列にプロパティ値を持たない複数値プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3912d-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3912d-125">解説</span><span class="sxs-lookup"><span data-stu-id="3912d-125">Remarks</span></span>

<span data-ttu-id="3912d-126">_pcb_パラメーターで NULL が渡された場合、 **sccountprops**関数は通知の配列を検証しますが、カウントは行われません。</span><span class="sxs-lookup"><span data-stu-id="3912d-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="3912d-127">非 null 値が_pcb_で渡された場合、 **sccountnotifications**関数は配列のサイズを決定し、原因となった_pcb_を格納します。</span><span class="sxs-lookup"><span data-stu-id="3912d-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="3912d-128">_pcb_パラメーターは、配列全体を格納するのに十分な大きさである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3912d-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="3912d-129">カウントすると、 **sccountprops**は配列に関連付けられているメモリを検証します。</span><span class="sxs-lookup"><span data-stu-id="3912d-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="3912d-130">**sccountprops**は、どの MAPI が情報を持っているかに関するプロパティでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="3912d-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3912d-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="3912d-131">See also</span></span>



[<span data-ttu-id="3912d-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="3912d-132">PropCopyMore</span></span>](propcopymore.md)

