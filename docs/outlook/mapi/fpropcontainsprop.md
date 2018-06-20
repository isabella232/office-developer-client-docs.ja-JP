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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: abf33e4167d836aeb88fdefb30ba05840e80ce63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800120"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="821d7-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="821d7-103">FPropContainsProp</span></span>

<span data-ttu-id="821d7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="821d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="821d7-105">文字列またはバイナリ配列は、1 つが含まれている他の一般的に、2 つのプロパティ値を比較します。</span><span class="sxs-lookup"><span data-stu-id="821d7-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="821d7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="821d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="821d7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="821d7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="821d7-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="821d7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="821d7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="821d7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="821d7-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="821d7-110">Called by:</span></span>  <br/> |<span data-ttu-id="821d7-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="821d7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="821d7-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="821d7-112">Parameters</span></span>

<span data-ttu-id="821d7-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="821d7-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="821d7-114">[in]_LpSPropValueSrc_パラメーターで指定された検索文字列を含む可能性があるプロパティの値を定義する[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="821d7-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="821d7-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="821d7-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="821d7-116">[in]_LpSPropValueDst_パラメーターで指定されたプロパティの値で**FPropContainsProp**を検索する検索文字列を定義する**SPropValue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="821d7-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="821d7-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="821d7-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="821d7-118">[in]オプションの設定 preciseness のレベルを定義する、比較で使用します。</span><span class="sxs-lookup"><span data-stu-id="821d7-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="821d7-119">**下位 16 ビット**は、PT_BINARY と PT_STRING8 型のプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="821d7-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="821d7-120">次の値の 1 つだけを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="821d7-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="821d7-121">FL_FULLSTRING: _lpSPropValueSrc_の検索文字列を_lpSPropValueDst_で識別されるプロパティの値と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="821d7-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="821d7-122">FL_PREFIX: _lpSPropValueSrc_の検索文字列は、 _lpSPropValueDst_によって識別されるプロパティの値の先頭にあります。</span><span class="sxs-lookup"><span data-stu-id="821d7-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="821d7-123">_LpSPropValueSrc_によって示される検索文字列の長さの分だけ、2 つの値を比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="821d7-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="821d7-124">FL_SUBSTRING: _lpSPropValueSrc_の検索文字列に含まれなければならない任意の場所_lpSPropValueDst_によって識別されるプロパティの値。</span><span class="sxs-lookup"><span data-stu-id="821d7-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="821d7-125">**上位 16 ビット**は PT_STRING8 の種類のプロパティにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="821d7-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="821d7-126">任意の組み合わせで次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="821d7-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="821d7-127">FL_IGNORECASE: 大文字と小文字を考慮せず、比較を行ってください。</span><span class="sxs-lookup"><span data-stu-id="821d7-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="821d7-128">FL_IGNORENONSPACE: 比較は、アクセント記号などの非スペーシング文字の Unicode で定義されているを無視してください。</span><span class="sxs-lookup"><span data-stu-id="821d7-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="821d7-129">FL_LOOSE: 比較が一致する限り、大文字と小文字を示す必要がありますと小文字を区別し、非スペーシング文字。</span><span class="sxs-lookup"><span data-stu-id="821d7-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="821d7-130">�߂�l</span><span class="sxs-lookup"><span data-stu-id="821d7-130">Return value</span></span>

<span data-ttu-id="821d7-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="821d7-131">TRUE</span></span> 
  
> <span data-ttu-id="821d7-132">パラメーターはすべて有効ですし、 _lpSPropValueSrc_の検索文字列が含まれている_lpSPropValueDst_プロパティの値で指定しました。</span><span class="sxs-lookup"><span data-stu-id="821d7-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="821d7-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="821d7-133">FALSE</span></span> 
  
> <span data-ttu-id="821d7-134">PT_STRING8 または PT_BINARY 型は比較対象のプロパティ値、プロパティ値は、さまざまな種類のまたは_lpSPropValueSrc_の検索文字列が含まれていない_lpSPropValueDst_のプロパティの値で指定しました。</span><span class="sxs-lookup"><span data-stu-id="821d7-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="821d7-135">備考</span><span class="sxs-lookup"><span data-stu-id="821d7-135">Remarks</span></span>

<span data-ttu-id="821d7-136">比較メソッドは、 [SPropValue](spropvalue.md)プロパティの定義で指定されたプロパティの型および_ulFuzzyLevel_パラメーターで指定したあいまいレベル ヒューリスティックによって異なります。</span><span class="sxs-lookup"><span data-stu-id="821d7-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="821d7-137">テーブルを生成するための制限を準備するのには、 [FPropCompareProp](fpropcompareprop.md)と**FPropContainsProp**関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="821d7-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="821d7-138">PT_BINARY プロパティの型では、 _ulFuzzyLevel_の上位 16 ビットは無視されます。</span><span class="sxs-lookup"><span data-stu-id="821d7-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="821d7-139">_UlFuzzyLevel_の設定が存在しないか無効な場合、完全な文字列の完全一致が実行されます。</span><span class="sxs-lookup"><span data-stu-id="821d7-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="821d7-140">プロパティの包含構造の詳細については、 [SContentRestriction](scontentrestriction.md)構造体を参照してください。</span><span class="sxs-lookup"><span data-stu-id="821d7-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

