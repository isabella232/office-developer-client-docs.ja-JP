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
description: 別のテキスト文字列に含まれる1つのテキスト文字列を検索し、その文字列を含む文字列の位置を基準にして、検索する文字列の開始位置を返します。
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322499"
---
# <a name="find-function"></a><span data-ttu-id="91ed5-103">FIND 関数</span><span class="sxs-lookup"><span data-stu-id="91ed5-103">FIND Function</span></span>

<span data-ttu-id="91ed5-104">別のテキスト文字列に含まれる1つのテキスト文字列を検索し、その文字列を含む文字列の位置を基準にして、検索する文字列の開始位置を返します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="91ed5-105">構文</span><span class="sxs-lookup"><span data-stu-id="91ed5-105">Syntax</span></span>

<span data-ttu-id="91ed5-106">find (\* \* \*\* 検索語 \* \*, \* \*\* \* 対象 \* *, [* **開始位置** *], [* \* *ignore_case* \* \*])</span><span class="sxs-lookup"><span data-stu-id="91ed5-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="91ed5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="91ed5-107">Parameters</span></span>

|<span data-ttu-id="91ed5-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="91ed5-108">**Name**</span></span>|<span data-ttu-id="91ed5-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="91ed5-109">**Required/Optional**</span></span>|<span data-ttu-id="91ed5-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="91ed5-110">**Data Type**</span></span>|<span data-ttu-id="91ed5-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="91ed5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="91ed5-112">_文字列_</span><span class="sxs-lookup"><span data-stu-id="91ed5-112">_find_text_</span></span> <br/> |<span data-ttu-id="91ed5-113">必須</span><span class="sxs-lookup"><span data-stu-id="91ed5-113">Required</span></span>  <br/> |<span data-ttu-id="91ed5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="91ed5-114">**String**</span></span> <br/> |<span data-ttu-id="91ed5-115">検索する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="91ed5-116">_format_</span><span class="sxs-lookup"><span data-stu-id="91ed5-116">_format_</span></span> <br/> |<span data-ttu-id="91ed5-117">必須</span><span class="sxs-lookup"><span data-stu-id="91ed5-117">Required</span></span>  <br/> |<span data-ttu-id="91ed5-118">**String**</span><span class="sxs-lookup"><span data-stu-id="91ed5-118">**String**</span></span> <br/> |<span data-ttu-id="91ed5-119">検索する文字列を含んでいる文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="91ed5-120">_開始_</span><span class="sxs-lookup"><span data-stu-id="91ed5-120">_start_num_</span></span> <br/> |<span data-ttu-id="91ed5-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="91ed5-121">Optional</span></span>  <br/> |<span data-ttu-id="91ed5-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="91ed5-122">**Number**</span></span> <br/> |<span data-ttu-id="91ed5-123">検索を開始する文字の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-123">The character at which to start the search.</span></span> <span data-ttu-id="91ed5-124">対象の最初の__ 文字は1です。</span><span class="sxs-lookup"><span data-stu-id="91ed5-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="91ed5-125">_開始位置_が指定されていない場合は、1と見なされます。</span><span class="sxs-lookup"><span data-stu-id="91ed5-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="91ed5-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="91ed5-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="91ed5-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="91ed5-127">Optional</span></span>  <br/> |<span data-ttu-id="91ed5-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="91ed5-128">**Boolean**</span></span> <br/> |<span data-ttu-id="91ed5-129">既定では、FIND 関数は大文字と小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="91ed5-130">大文字と小文字を区別しないようにするには、この引数の値を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="91ed5-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="91ed5-131">Return value</span></span>

<span data-ttu-id="91ed5-132">番号</span><span class="sxs-lookup"><span data-stu-id="91ed5-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91ed5-133">解説</span><span class="sxs-lookup"><span data-stu-id="91ed5-133">Remarks</span></span>

<span data-ttu-id="91ed5-134">一致する文字列が複数ある場合、FIND 関数は文字列内で最初に一致した文字列の開始位置を返します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="91ed5-135">"検索_文字列_" 引数では、ワイルドカードとして使用する文字は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="91ed5-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="91ed5-136">検索_文字列_の場合:</span><span class="sxs-lookup"><span data-stu-id="91ed5-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="91ed5-137">が空 ("") の場合、FIND は検索文字列の最初の文字 (つまり、_開始位置_または1の文字) と一致します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="91ed5-138">対象に含まれ__ ない場合、FIND は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="91ed5-139">が返されます。</span><span class="sxs-lookup"><span data-stu-id="91ed5-139">error value.</span></span> 
    
<span data-ttu-id="91ed5-140">_開始位置_:</span><span class="sxs-lookup"><span data-stu-id="91ed5-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="91ed5-141">start_num がゼロ (0) 以下の場合、FIND は #VALUE!</span><span class="sxs-lookup"><span data-stu-id="91ed5-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="91ed5-142">エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-142">error value.</span></span> 
    
- <span data-ttu-id="91ed5-143">が対象の長さより大きい__ 場合、findreturns #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="91ed5-144">が返されます。</span><span class="sxs-lookup"><span data-stu-id="91ed5-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="91ed5-145">例</span><span class="sxs-lookup"><span data-stu-id="91ed5-145">Example</span></span>

<span data-ttu-id="91ed5-146">FIND ("2003","January 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="91ed5-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="91ed5-147">12 を返します。</span><span class="sxs-lookup"><span data-stu-id="91ed5-147">Returns 12.</span></span> 
  

