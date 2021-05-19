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
# <a name="fpropcontainsprop"></a><span data-ttu-id="1bb39-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="1bb39-103">FPropContainsProp</span></span>

<span data-ttu-id="1bb39-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bb39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bb39-105">2 つのプロパティ値 (通常は文字列またはバイナリ配列) を比較して、もう 1 つのプロパティ値にもう一方が含まれているか確認します。</span><span class="sxs-lookup"><span data-stu-id="1bb39-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bb39-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1bb39-106">Header file:</span></span>  <br/> |<span data-ttu-id="1bb39-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1bb39-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1bb39-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="1bb39-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1bb39-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1bb39-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1bb39-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="1bb39-110">Called by:</span></span>  <br/> |<span data-ttu-id="1bb39-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1bb39-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="1bb39-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1bb39-112">Parameters</span></span>

<span data-ttu-id="1bb39-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="1bb39-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="1bb39-114">[in]_lpSPropValueSrc_ パラメーターが指す検索文字列を含む可能性があるプロパティ値を定義する [SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1bb39-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="1bb39-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="1bb39-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="1bb39-116">[in]_lpSPropValueDst_ パラメーターが指すプロパティ値で **FPropContainsProp** がシークしている検索文字列を定義する **SPropValue** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1bb39-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="1bb39-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="1bb39-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="1bb39-118">[in]比較で使用する精度のレベルを定義するオプション設定。</span><span class="sxs-lookup"><span data-stu-id="1bb39-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="1bb39-119">下位 **16 ビットは、** 種類と種類のプロパティに適用PT_BINARYおよびPT_STRING8。</span><span class="sxs-lookup"><span data-stu-id="1bb39-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="1bb39-120">これらは、次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="1bb39-121">FL_FULLSTRING:  _lpSPropValueSrc_ 検索文字列は  _、lpSPropValueDst_ で識別されるプロパティ値と等しくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="1bb39-122">FL_PREFIX:  _lpSPropValueSrc_ 検索文字列は  _、lpSPropValueDst_ で識別されるプロパティ値の先頭に表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="1bb39-123">2 つの値は  _、lpSPropValueSrc_ で示される検索文字列の長さまでのみ比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="1bb39-124">FL_SUBSTRING:  _lpSPropValueSrc_ 検索文字列は  _、lpSPropValueDst_ で識別されるプロパティ値の任意の場所に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="1bb39-125">上位 **16 ビットは、** データ型のプロパティにのみPT_STRING8。</span><span class="sxs-lookup"><span data-stu-id="1bb39-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="1bb39-126">これらは、任意の組み合わせで次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1bb39-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="1bb39-127">FL_IGNORECASE: 大文字と小文字の区別を考慮せずに比較を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="1bb39-128">FL_IGNORENONSPACE: この比較では、Unicode で定義された非太平洋文字 (等値記号など) は無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="1bb39-129">FL_LOOSE: 大文字と小文字の区別と非スパック文字を無視して、可能な限り一致を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1bb39-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="1bb39-130">Return value</span></span>

<span data-ttu-id="1bb39-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="1bb39-131">TRUE</span></span> 
  
> <span data-ttu-id="1bb39-132">パラメーターはすべて有効で  _、lpSPropValueSrc_ 検索文字列は  _lpSPropValueDst_ プロパティの値で指定されている通り含まれています。</span><span class="sxs-lookup"><span data-stu-id="1bb39-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="1bb39-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="1bb39-133">FALSE</span></span> 
  
> <span data-ttu-id="1bb39-134">比較されるプロパティの値は、PT_STRING8 または PT_BINARY 型ではないか、プロパティ値が異なる型か  _、lpSPropValueSrc_ 検索文字列が  _lpSPropValueDst_ プロパティ値で指定された値に含めされていません。</span><span class="sxs-lookup"><span data-stu-id="1bb39-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1bb39-135">注釈</span><span class="sxs-lookup"><span data-stu-id="1bb39-135">Remarks</span></span>

<span data-ttu-id="1bb39-136">比較メソッドは [、SPropValue](spropvalue.md) プロパティ定義で指定されたプロパティの種類と  _、ulFuzzyLevel_ パラメーターで提供されるファジー レベルのヒューリスティックによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1bb39-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="1bb39-137">[FPropCompareProp](fpropcompareprop.md)関数と **FPropContainsProp** 関数を使用して、テーブルを生成するための制限を準備できます。</span><span class="sxs-lookup"><span data-stu-id="1bb39-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="1bb39-138">_ulFuzzyLevel_ の上位 16 ビットは、プロパティの種類が指定PT_BINARY。</span><span class="sxs-lookup"><span data-stu-id="1bb39-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="1bb39-139">_ulFuzzyLevel の設定が_ 見つからないか無効な場合は、完全文字列の完全一致が実行されます。</span><span class="sxs-lookup"><span data-stu-id="1bb39-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="1bb39-140">プロパティの格納の詳細については [、「SContentRestriction 構造体」を参照](scontentrestriction.md) してください。</span><span class="sxs-lookup"><span data-stu-id="1bb39-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

