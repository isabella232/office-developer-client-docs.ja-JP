---
title: FIND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: 別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、それを含むテキスト文字列内の位置を基準にして検索するテキスト文字列の開始位置を返します。
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805413"
---
# <a name="find-function"></a><span data-ttu-id="69a63-103">FIND 関数</span><span class="sxs-lookup"><span data-stu-id="69a63-103">FIND Function</span></span>

<span data-ttu-id="69a63-104">別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、それを含むテキスト文字列内の位置を基準にして検索するテキスト文字列の開始位置を返します。</span><span class="sxs-lookup"><span data-stu-id="69a63-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="69a63-105">構文</span><span class="sxs-lookup"><span data-stu-id="69a63-105">Syntax</span></span>

<span data-ttu-id="69a63-106">検索 (* **文字列** *、* **対象** *、[* **開始** *]、[* * *ignore_case* * *])</span><span class="sxs-lookup"><span data-stu-id="69a63-106">FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="69a63-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="69a63-107">Parameters</span></span>

|<span data-ttu-id="69a63-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="69a63-108">**Name**</span></span>|<span data-ttu-id="69a63-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="69a63-109">**Required/Optional**</span></span>|<span data-ttu-id="69a63-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="69a63-110">**Data Type**</span></span>|<span data-ttu-id="69a63-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="69a63-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="69a63-112">_検索文字列_</span><span class="sxs-lookup"><span data-stu-id="69a63-112">_find_text_</span></span> <br/> |<span data-ttu-id="69a63-113">必須</span><span class="sxs-lookup"><span data-stu-id="69a63-113">Required</span></span>  <br/> |<span data-ttu-id="69a63-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="69a63-114">**String**</span></span> <br/> |<span data-ttu-id="69a63-115">検索する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="69a63-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="69a63-116">_format_</span><span class="sxs-lookup"><span data-stu-id="69a63-116">_format_</span></span> <br/> |<span data-ttu-id="69a63-117">必須</span><span class="sxs-lookup"><span data-stu-id="69a63-117">Required</span></span>  <br/> |<span data-ttu-id="69a63-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="69a63-118">**String**</span></span> <br/> |<span data-ttu-id="69a63-119">検索する文字列を含んでいる文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="69a63-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="69a63-120">_開始位置_</span><span class="sxs-lookup"><span data-stu-id="69a63-120">_start_num_</span></span> <br/> |<span data-ttu-id="69a63-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="69a63-121">Optional</span></span>  <br/> |<span data-ttu-id="69a63-122">**番号**</span><span class="sxs-lookup"><span data-stu-id="69a63-122">**Number**</span></span> <br/> |<span data-ttu-id="69a63-123">文字の検索を開始する位置。</span><span class="sxs-lookup"><span data-stu-id="69a63-123">The character at which to start the search.</span></span> <span data-ttu-id="69a63-124">_対象_の最初の文字は、1 です。</span><span class="sxs-lookup"><span data-stu-id="69a63-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="69a63-125">_開始位置_が指定されていない場合は 1 であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="69a63-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="69a63-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="69a63-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="69a63-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="69a63-127">Optional</span></span>  <br/> |<span data-ttu-id="69a63-128">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="69a63-128">**Boolean**</span></span> <br/> |<span data-ttu-id="69a63-p102">既定では、FIND 関数は大文字と小文字を区別します。大文字と小文字を区別しないようにするには、この引数の値を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="69a63-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="69a63-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="69a63-131">Return value</span></span>

<span data-ttu-id="69a63-132">数値</span><span class="sxs-lookup"><span data-stu-id="69a63-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69a63-133">備考</span><span class="sxs-lookup"><span data-stu-id="69a63-133">Remarks</span></span>

<span data-ttu-id="69a63-134">複数の一致が見つかった場合、FIND 関数は、文字列に一致する最初の開始位置を返します。</span><span class="sxs-lookup"><span data-stu-id="69a63-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="69a63-135">_文字列_引数には、ワイルドカードを使用する任意の文字は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="69a63-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="69a63-136">場合_文字列を指定_します。</span><span class="sxs-lookup"><span data-stu-id="69a63-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="69a63-137">空 ("")、検索に一致する検索文字列の最初の文字 (つまり、文字番号_開始位置_または 1)。</span><span class="sxs-lookup"><span data-stu-id="69a63-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="69a63-138">ない_対象_検索、#VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="69a63-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="69a63-139">エラー値です。</span><span class="sxs-lookup"><span data-stu-id="69a63-139">error value.</span></span> 
    
<span data-ttu-id="69a63-140">場合_開始位置_。</span><span class="sxs-lookup"><span data-stu-id="69a63-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="69a63-p105">start_num がゼロ (0) 以下の場合、FIND は #VALUE! エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="69a63-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="69a63-143">_対象_#VALUE を FINDreturns の長さを超える値です。</span><span class="sxs-lookup"><span data-stu-id="69a63-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="69a63-144">エラー値です。</span><span class="sxs-lookup"><span data-stu-id="69a63-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="69a63-145">例</span><span class="sxs-lookup"><span data-stu-id="69a63-145">Example</span></span>

<span data-ttu-id="69a63-146">FIND ("2003","January 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="69a63-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="69a63-147">12 を返します。</span><span class="sxs-lookup"><span data-stu-id="69a63-147">Returns 12.</span></span> 
  

