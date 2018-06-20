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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 69bbed644a8173bf9291ca48a63960f693108318
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800116"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="e9912-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="e9912-103">FPropCompareProp</span></span>

<span data-ttu-id="e9912-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9912-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9912-105">指定したリレーショナル演算子を使用して 2 つのプロパティ値を比較します。</span><span class="sxs-lookup"><span data-stu-id="e9912-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9912-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e9912-106">Header file:</span></span>  <br/> |<span data-ttu-id="e9912-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e9912-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e9912-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e9912-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e9912-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e9912-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e9912-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e9912-110">Called by:</span></span>  <br/> |<span data-ttu-id="e9912-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9912-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="e9912-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e9912-112">Parameters</span></span>

<span data-ttu-id="e9912-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="e9912-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="e9912-114">[in]比較のための最初のプロパティ値を定義する[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9912-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="e9912-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="e9912-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="e9912-116">[in]比較で使用する関係演算子です。</span><span class="sxs-lookup"><span data-stu-id="e9912-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="e9912-117">許容値は、 [SComparePropsRestriction](scomparepropsrestriction.md)構造体を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9912-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="e9912-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="e9912-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="e9912-119">[in]**SPropValue**構造体の比較の 2 番目のプロパティの値を定義することへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9912-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e9912-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e9912-120">Return value</span></span>

<span data-ttu-id="e9912-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="e9912-121">TRUE</span></span> 
  
> <span data-ttu-id="e9912-122">プロパティの値は、指定された関係を満たします。</span><span class="sxs-lookup"><span data-stu-id="e9912-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="e9912-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="e9912-123">FALSE</span></span> 
  
> <span data-ttu-id="e9912-124">プロパティの値は、指定したリレーションシップを満たしていません。</span><span class="sxs-lookup"><span data-stu-id="e9912-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9912-125">備考</span><span class="sxs-lookup"><span data-stu-id="e9912-125">Remarks</span></span>

<span data-ttu-id="e9912-126">比較メソッドは、 [SPropValue](spropvalue.md)プロパティの定義で指定されたプロパティの型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e9912-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="e9912-127">テーブルを生成するための制限を準備するのには、 **FPropCompareProp**と[FPropContainsProp](fpropcontainsprop.md)関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e9912-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="e9912-128">比較の順序は、 _lpSPropValue1_、_ ulRelOp _ _ lpSPropValue2 _ です。</span><span class="sxs-lookup"><span data-stu-id="e9912-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="e9912-129">比較するプロパティの値のプロパティの型が一致しない場合、 **FPropCompareProp**関数は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="e9912-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

