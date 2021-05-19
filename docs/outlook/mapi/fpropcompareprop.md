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
# <a name="fpropcompareprop"></a><span data-ttu-id="21c6c-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="21c6c-103">FPropCompareProp</span></span>

<span data-ttu-id="21c6c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21c6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21c6c-105">指定した関係演算子を使用して 2 つのプロパティ値を比較します。</span><span class="sxs-lookup"><span data-stu-id="21c6c-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21c6c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="21c6c-106">Header file:</span></span>  <br/> |<span data-ttu-id="21c6c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="21c6c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="21c6c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="21c6c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="21c6c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="21c6c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="21c6c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="21c6c-110">Called by:</span></span>  <br/> |<span data-ttu-id="21c6c-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="21c6c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="21c6c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21c6c-112">Parameters</span></span>

<span data-ttu-id="21c6c-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="21c6c-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="21c6c-114">[in]比較の最初 [のプロパティ値](spropvalue.md) を定義する SPropValue 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="21c6c-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="21c6c-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="21c6c-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="21c6c-116">[in]比較で使用する関係演算子。</span><span class="sxs-lookup"><span data-stu-id="21c6c-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="21c6c-117">許容値については [、「SComparePropsRestriction 構造体」を参照](scomparepropsrestriction.md) してください。</span><span class="sxs-lookup"><span data-stu-id="21c6c-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="21c6c-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="21c6c-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="21c6c-119">[in]比較用の **2 番目の** プロパティ値を定義する SPropValue 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="21c6c-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="21c6c-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="21c6c-120">Return value</span></span>

<span data-ttu-id="21c6c-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="21c6c-121">TRUE</span></span> 
  
> <span data-ttu-id="21c6c-122">プロパティの値は、指定された関係を満たします。</span><span class="sxs-lookup"><span data-stu-id="21c6c-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="21c6c-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="21c6c-123">FALSE</span></span> 
  
> <span data-ttu-id="21c6c-124">プロパティの値は、指定された関係を満たさない。</span><span class="sxs-lookup"><span data-stu-id="21c6c-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21c6c-125">注釈</span><span class="sxs-lookup"><span data-stu-id="21c6c-125">Remarks</span></span>

<span data-ttu-id="21c6c-126">比較メソッドは [、SPropValue](spropvalue.md) プロパティ定義で指定されたプロパティの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="21c6c-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="21c6c-127">**FPropCompareProp** 関数と [FPropContainsProp](fpropcontainsprop.md)関数を使用して、テーブルを生成するための制限を準備できます。</span><span class="sxs-lookup"><span data-stu-id="21c6c-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="21c6c-128">比較の順序は  _lpSPropValue1_、 _ ulRelOp _, _ lpSPropValue2 _です。</span><span class="sxs-lookup"><span data-stu-id="21c6c-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="21c6c-129">比較するプロパティ値のプロパティの種類が一致しない場合 **、FPropCompareProp** 関数は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="21c6c-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

