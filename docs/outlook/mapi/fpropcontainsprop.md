---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432633"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="92ec6-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="92ec6-103">FPropContainsProp</span></span>

<span data-ttu-id="92ec6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92ec6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92ec6-105">2つのプロパティ値 (通常は文字列またはバイナリ配列) を比較して、一方に他方が含まれているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="92ec6-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92ec6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="92ec6-106">Header file:</span></span>  <br/> |<span data-ttu-id="92ec6-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="92ec6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="92ec6-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="92ec6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="92ec6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="92ec6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="92ec6-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="92ec6-110">Called by:</span></span>  <br/> |<span data-ttu-id="92ec6-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="92ec6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="92ec6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92ec6-112">Parameters</span></span>

<span data-ttu-id="92ec6-113">_lpspropvaluedst_</span><span class="sxs-lookup"><span data-stu-id="92ec6-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="92ec6-114">順番_lpspropバリュー rc_パラメーターで指定された検索文字列を含むことができるプロパティ値を定義する[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="92ec6-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="92ec6-115">_lpspropて rc_</span><span class="sxs-lookup"><span data-stu-id="92ec6-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="92ec6-116">順番**fpropan prop**が、 _lpspropvaluedst_パラメーターで指定されたプロパティ値をシークする、 **spropvalue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="92ec6-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="92ec6-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="92ec6-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="92ec6-118">順番比較で使用する preciseness のレベルを定義するオプション設定。</span><span class="sxs-lookup"><span data-stu-id="92ec6-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="92ec6-119">**下位16ビット**は、PT_BINARY および PT_STRING8 型のプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="92ec6-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="92ec6-120">次の値のいずれかを正確に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92ec6-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="92ec6-121">FL_FULLSTRING: _lpspropvalues rc_検索文字列は、 _lpspropvaluedst_で識別されるプロパティ値と等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="92ec6-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="92ec6-122">FL_PREFIX: lpspropvaluesrc の検索文字列は、 _lpspropvaluedst_で識別されるプロパティ値の先頭に配置する必要があります。 __</span><span class="sxs-lookup"><span data-stu-id="92ec6-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="92ec6-123">2つの値は、 _lpspropvalues rc_で示される検索文字列の長さまで比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92ec6-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="92ec6-124">FL_SUBSTRING: lpspropvaluesrc の検索文字列は、 _lpspropvaluedst_で識別されるプロパティ値の任意の場所に格納されている必要があります。 __</span><span class="sxs-lookup"><span data-stu-id="92ec6-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="92ec6-125">**上位16ビット**は、PT_STRING8 型のプロパティにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="92ec6-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="92ec6-126">これらの値は、次の任意の組み合わせで設定できます。</span><span class="sxs-lookup"><span data-stu-id="92ec6-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="92ec6-127">FL_IGNORECASE: 比較は大文字と小文字の区別を考慮せずに行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="92ec6-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="92ec6-128">FL_IGNORENONSPACE: 比較では、Unicode で定義されたスペーシング文字 (アクセント記号など) を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92ec6-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="92ec6-129">FL_LOOSE: 比較では、大文字と小文字の区別を無視して、可能な限り一致を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="92ec6-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="92ec6-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="92ec6-130">Return value</span></span>

<span data-ttu-id="92ec6-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="92ec6-131">TRUE</span></span> 
  
> <span data-ttu-id="92ec6-132">パラメーターはすべて有効で、lpspropvaluesrc の検索文字列は_lpspropvaluedst_プロパティ値に指定されたとおりに含まれています。 __</span><span class="sxs-lookup"><span data-stu-id="92ec6-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="92ec6-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="92ec6-133">FALSE</span></span> 
  
> <span data-ttu-id="92ec6-134">比較対象のプロパティ値が PT_STRING8 または PT_BINARY の型ではないか、プロパティ値が異なる型で__ あるか、lpspropvaluesrc 検索文字列が_lpspropvaluedst_プロパティ値で指定されたとおりに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="92ec6-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="92ec6-135">注釈</span><span class="sxs-lookup"><span data-stu-id="92ec6-135">Remarks</span></span>

<span data-ttu-id="92ec6-136">比較方法は、 [spropvalue](spropvalue.md)プロパティの定義に指定されているプロパティの種類と、 _ulFuzzyLevel_パラメーターで指定されているファジーレベルヒューリスティックによって異なります。</span><span class="sxs-lookup"><span data-stu-id="92ec6-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="92ec6-137">[fpropcompareprop](fpropcompareprop.md)および**fpropの prop**関数を使用して、テーブルの生成に関する制限を準備できます。</span><span class="sxs-lookup"><span data-stu-id="92ec6-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="92ec6-138">プロパティの種類が PT_BINARY の場合、 _ulFuzzyLevel_の上位16ビットは無視されます。</span><span class="sxs-lookup"><span data-stu-id="92ec6-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="92ec6-139">_ulFuzzyLevel_の設定が指定されていない場合、または無効な場合は、完全な文字列の完全一致が実行されます。</span><span class="sxs-lookup"><span data-stu-id="92ec6-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="92ec6-140">プロパティコンテインメントの詳細については、 [scontentrestriction](scontentrestriction.md)構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92ec6-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

