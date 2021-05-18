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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404975"
---
# <a name="sccountprops"></a><span data-ttu-id="e0387-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="e0387-103">ScCountProps</span></span>

  
  
<span data-ttu-id="e0387-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0387-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0387-105">プロパティ値配列のサイズ (バイト単位) を決定し、配列に関連付けられているメモリを検証します。</span><span class="sxs-lookup"><span data-stu-id="e0387-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0387-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e0387-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0387-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e0387-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e0387-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e0387-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e0387-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e0387-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e0387-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e0387-110">Called by:</span></span>  <br/> |<span data-ttu-id="e0387-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e0387-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="e0387-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e0387-112">Parameters</span></span>

 <span data-ttu-id="e0387-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="e0387-113">_cprop_</span></span>
  
> <span data-ttu-id="e0387-114">[in]  _rgprop_ パラメーターで示される配列内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="e0387-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="e0387-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="e0387-115">_rgprop_</span></span>
  
> <span data-ttu-id="e0387-116">[in]サイズを決定するプロパティを定義する [SPropValue](spropvalue.md) 構造体の配列内の範囲へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e0387-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="e0387-117">この範囲は必ずしも配列の先頭から始まるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="e0387-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="e0387-118">_pcb_</span><span class="sxs-lookup"><span data-stu-id="e0387-118">_pcb_</span></span>
  
> <span data-ttu-id="e0387-119">[out]プロパティ配列のサイズ (バイト単位) へのオプションのポインター。</span><span class="sxs-lookup"><span data-stu-id="e0387-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0387-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="e0387-120">Return value</span></span>

<span data-ttu-id="e0387-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0387-121">S_OK</span></span> 
  
> <span data-ttu-id="e0387-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e0387-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e0387-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0387-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e0387-124">プロパティ値配列内の少なくとも 1 つのプロパティに PROP_ID_NULL または PROP_ID_INVALID の識別子が含まれているか、プロパティ配列にプロパティ値がない複数値プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e0387-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0387-125">注釈</span><span class="sxs-lookup"><span data-stu-id="e0387-125">Remarks</span></span>

<span data-ttu-id="e0387-126">NULL が pcbパラメーターで渡された場合 **、ScCountProps** 関数は通知の配列を検証しますが、カウントは実行されません。</span><span class="sxs-lookup"><span data-stu-id="e0387-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="e0387-127">null 以外の値が  _pcb_ で渡された場合 **、ScCountNotifications** 関数は配列のサイズを決定し、原因  _の pcb_ を格納します。</span><span class="sxs-lookup"><span data-stu-id="e0387-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="e0387-128">pcb  _パラメーターは_ 、配列全体を格納するのに十分な大きい値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0387-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="e0387-129">カウント中に **、ScCountProps は** 配列に関連付けられたメモリを検証します。</span><span class="sxs-lookup"><span data-stu-id="e0387-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="e0387-130">**ScCountProps は** 、MAPI に関する情報を持つプロパティでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="e0387-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0387-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0387-131">See also</span></span>



[<span data-ttu-id="e0387-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="e0387-132">PropCopyMore</span></span>](propcopymore.md)

