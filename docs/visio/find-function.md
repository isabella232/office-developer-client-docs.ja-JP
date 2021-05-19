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
description: 別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、その文字列を含むテキスト文字列内の位置を基準に検索するテキスト文字列の開始位置を返します。
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426577"
---
# <a name="find-function"></a><span data-ttu-id="b6cc0-103">FIND 関数</span><span class="sxs-lookup"><span data-stu-id="b6cc0-103">FIND Function</span></span>

<span data-ttu-id="b6cc0-104">別のテキスト文字列内に含まれる 1 つのテキスト文字列を検索し、その文字列を含むテキスト文字列内の位置を基準に検索するテキスト文字列の開始位置を返します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b6cc0-105">構文</span><span class="sxs-lookup"><span data-stu-id="b6cc0-105">Syntax</span></span>

<span data-ttu-id="b6cc0-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\*\*\* ignore_case \*\* ])</span><span class="sxs-lookup"><span data-stu-id="b6cc0-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b6cc0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6cc0-107">Parameters</span></span>

|<span data-ttu-id="b6cc0-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-108">**Name**</span></span>|<span data-ttu-id="b6cc0-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-109">**Required/Optional**</span></span>|<span data-ttu-id="b6cc0-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-110">**Data Type**</span></span>|<span data-ttu-id="b6cc0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b6cc0-112">_find_text_</span><span class="sxs-lookup"><span data-stu-id="b6cc0-112">_find_text_</span></span> <br/> |<span data-ttu-id="b6cc0-113">必須</span><span class="sxs-lookup"><span data-stu-id="b6cc0-113">Required</span></span>  <br/> |<span data-ttu-id="b6cc0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-114">**String**</span></span> <br/> |<span data-ttu-id="b6cc0-115">検索する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="b6cc0-116">_format_</span><span class="sxs-lookup"><span data-stu-id="b6cc0-116">_format_</span></span> <br/> |<span data-ttu-id="b6cc0-117">必須</span><span class="sxs-lookup"><span data-stu-id="b6cc0-117">Required</span></span>  <br/> |<span data-ttu-id="b6cc0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-118">**String**</span></span> <br/> |<span data-ttu-id="b6cc0-119">検索する文字列を含んでいる文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="b6cc0-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="b6cc0-120">_start_num_</span></span> <br/> |<span data-ttu-id="b6cc0-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="b6cc0-121">Optional</span></span>  <br/> |<span data-ttu-id="b6cc0-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-122">**Number**</span></span> <br/> |<span data-ttu-id="b6cc0-123">検索を開始する文字の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-123">The character at which to start the search.</span></span> <span data-ttu-id="b6cc0-124">この値の最初  _のwithin_text_ は 1 です。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="b6cc0-125">この  _start_num_ 見つからない場合は、1 と見なされます。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="b6cc0-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="b6cc0-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="b6cc0-127">省略可能</span><span class="sxs-lookup"><span data-stu-id="b6cc0-127">Optional</span></span>  <br/> |<span data-ttu-id="b6cc0-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b6cc0-128">**Boolean**</span></span> <br/> |<span data-ttu-id="b6cc0-p102">既定では、FIND 関数は大文字と小文字を区別します。大文字と小文字を区別しないようにするには、この引数の値を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b6cc0-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="b6cc0-131">Return value</span></span>

<span data-ttu-id="b6cc0-132">番号</span><span class="sxs-lookup"><span data-stu-id="b6cc0-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6cc0-133">注釈</span><span class="sxs-lookup"><span data-stu-id="b6cc0-133">Remarks</span></span>

<span data-ttu-id="b6cc0-134">一致する文字列が複数ある場合、FIND 関数は文字列内で最初に一致した文字列の開始位置を返します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="b6cc0-135">引数  _find_text_ は、任意の文字をワイルドカードと見なしません。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="b6cc0-136">次 _find_text:_</span><span class="sxs-lookup"><span data-stu-id="b6cc0-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="b6cc0-137">空 ("") の場合、FIND は検索文字列の最初の文字 (つまり、番号が 1 または 1)  _start_num_ 一致します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="b6cc0-138">ファイルに表示されない  _場合within_text_ FIND は、次の#VALUE。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="b6cc0-139">が返されます。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-139">error value.</span></span> 
    
<span data-ttu-id="b6cc0-140">次 _start_num:_</span><span class="sxs-lookup"><span data-stu-id="b6cc0-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="b6cc0-p105">start_num がゼロ (0) 以下の場合、FIND は #VALUE! エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="b6cc0-143">値の長さ  _より大きい_ 場合、FINDreturns within_textを返#VALUE!</span><span class="sxs-lookup"><span data-stu-id="b6cc0-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="b6cc0-144">が返されます。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="b6cc0-145">例</span><span class="sxs-lookup"><span data-stu-id="b6cc0-145">Example</span></span>

<span data-ttu-id="b6cc0-146">FIND ("2003","January 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="b6cc0-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="b6cc0-147">12 を返します。</span><span class="sxs-lookup"><span data-stu-id="b6cc0-147">Returns 12.</span></span> 
  

