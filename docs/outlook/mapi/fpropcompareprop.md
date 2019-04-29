---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427158"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="8291f-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="8291f-103">FPropCompareProp</span></span>

<span data-ttu-id="8291f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8291f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8291f-105">指定した関係演算子を使用して、2つのプロパティの値を比較します。</span><span class="sxs-lookup"><span data-stu-id="8291f-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8291f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8291f-106">Header file:</span></span>  <br/> |<span data-ttu-id="8291f-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="8291f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8291f-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="8291f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8291f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8291f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8291f-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="8291f-110">Called by:</span></span>  <br/> |<span data-ttu-id="8291f-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="8291f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="8291f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8291f-112">Parameters</span></span>

<span data-ttu-id="8291f-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="8291f-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="8291f-114">順番比較のための最初のプロパティ値を定義する[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8291f-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="8291f-115">_ulrelop_</span><span class="sxs-lookup"><span data-stu-id="8291f-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="8291f-116">順番比較で使用する関係演算子を示します。</span><span class="sxs-lookup"><span data-stu-id="8291f-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="8291f-117">許容値については、 [scomparepropsrestriction](scomparepropsrestriction.md)構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8291f-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="8291f-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="8291f-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="8291f-119">順番比較の2番目のプロパティの値を定義する**spropvalue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8291f-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8291f-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="8291f-120">Return value</span></span>

<span data-ttu-id="8291f-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="8291f-121">TRUE</span></span> 
  
> <span data-ttu-id="8291f-122">プロパティ値は、指定されたリレーションを満たします。</span><span class="sxs-lookup"><span data-stu-id="8291f-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="8291f-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="8291f-123">FALSE</span></span> 
  
> <span data-ttu-id="8291f-124">プロパティの値は、指定されたリレーションシップを満たしていません。</span><span class="sxs-lookup"><span data-stu-id="8291f-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8291f-125">注釈</span><span class="sxs-lookup"><span data-stu-id="8291f-125">Remarks</span></span>

<span data-ttu-id="8291f-126">比較方法は、 [spropvalue](spropvalue.md)プロパティの定義で指定されているプロパティの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8291f-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="8291f-127">**fpropcompareprop**および[fpropの prop](fpropcontainsprop.md)関数を使用して、テーブルの生成に関する制限を準備できます。</span><span class="sxs-lookup"><span data-stu-id="8291f-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="8291f-128">比較の順序は_lpSPropValue1_、_ ulrelop _、_ lpSPropValue2 _ です。</span><span class="sxs-lookup"><span data-stu-id="8291f-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="8291f-129">比較するプロパティ値のプロパティの種類が一致しない場合、 **fpropcompareprop**関数は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="8291f-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

