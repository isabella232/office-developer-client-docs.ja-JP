---
title: SUBSTITUTE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: 文字列の一部を別の文字列に置き換えます。
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346824"
---
# <a name="substitute-function"></a><span data-ttu-id="3e1cb-103">SUBSTITUTE 関数</span><span class="sxs-lookup"><span data-stu-id="3e1cb-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="3e1cb-104">文字列の一部を別の文字列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3e1cb-105">構文</span><span class="sxs-lookup"><span data-stu-id="3e1cb-105">Syntax</span></span>

 <span data-ttu-id="3e1cb-106">代替 (\* \* *text* \* \*, \* **文字列** \*, \* **置換** \* [, \* **開始位置** \*] [, \* \* *ignore_case_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3e1cb-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3e1cb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3e1cb-107">Parameters</span></span>

|<span data-ttu-id="3e1cb-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-108">**Name**</span></span>|<span data-ttu-id="3e1cb-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-109">**Required/Optional**</span></span>|<span data-ttu-id="3e1cb-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-110">**Data Type**</span></span>|<span data-ttu-id="3e1cb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3e1cb-112">_text_</span><span class="sxs-lookup"><span data-stu-id="3e1cb-112">_text_</span></span> <br/> |<span data-ttu-id="3e1cb-113">必須</span><span class="sxs-lookup"><span data-stu-id="3e1cb-113">Required</span></span>  <br/> |<span data-ttu-id="3e1cb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-114">**String**</span></span> <br/> | <span data-ttu-id="3e1cb-115">文字を置換する文字列または文字列を含むセルへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="3e1cb-116">_文字列_</span><span class="sxs-lookup"><span data-stu-id="3e1cb-116">_old_text_</span></span> <br/> |<span data-ttu-id="3e1cb-117">必須</span><span class="sxs-lookup"><span data-stu-id="3e1cb-117">Required</span></span>  <br/> |<span data-ttu-id="3e1cb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-118">**String**</span></span> <br/> | <span data-ttu-id="3e1cb-119">置換する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="3e1cb-120">_文字列_</span><span class="sxs-lookup"><span data-stu-id="3e1cb-120">_new_text_</span></span> <br/> |<span data-ttu-id="3e1cb-121">必須</span><span class="sxs-lookup"><span data-stu-id="3e1cb-121">Required</span></span>  <br/> |<span data-ttu-id="3e1cb-122">**String**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-122">**String**</span></span> <br/> | <span data-ttu-id="3e1cb-123">文字列を置換するために使用する__ 文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="3e1cb-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="3e1cb-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="3e1cb-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="3e1cb-125">Optional</span></span>  <br/> |<span data-ttu-id="3e1cb-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-126">**Numeric**</span></span> <br/> |<span data-ttu-id="3e1cb-127">置換する文字列の出現を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="3e1cb-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="3e1cb-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="3e1cb-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="3e1cb-129">Optional</span></span>  <br/> |<span data-ttu-id="3e1cb-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-130">**Boolean**</span></span> <br/> |<span data-ttu-id="3e1cb-131">大文字と小文字を区別する場合は FALSE。それ以外の場合は TRUE。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="3e1cb-132">既定値は "FALSE" です。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3e1cb-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="3e1cb-133">Return value</span></span>

<span data-ttu-id="3e1cb-134">文字列</span><span class="sxs-lookup"><span data-stu-id="3e1cb-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e1cb-135">注釈</span><span class="sxs-lookup"><span data-stu-id="3e1cb-135">Remarks</span></span>

 <span data-ttu-id="3e1cb-136">_start_num_opt_を指定すると、指定した_文字列_だけが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="3e1cb-137">それ以外の場合は__ 、_テキスト_内のすべての検索文字列が置換文字列に変更され_ます。_</span><span class="sxs-lookup"><span data-stu-id="3e1cb-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="3e1cb-138">文字列内の特定のテキストを置換する場合は、代替関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="3e1cb-139">文字列内の特定の位置にある文字列を置換する場合は、replace 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="3e1cb-140">例</span><span class="sxs-lookup"><span data-stu-id="3e1cb-140">Example</span></span>

<span data-ttu-id="3e1cb-141">代用 ("1 年1月 2003", "january", "JAN", "JAN")</span><span class="sxs-lookup"><span data-stu-id="3e1cb-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="3e1cb-142">"1 JAN 2003" を返します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="3e1cb-143">代替 ("1 月 2003"、"january"、"JAN", "JAN")</span><span class="sxs-lookup"><span data-stu-id="3e1cb-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="3e1cb-144">"1 January 2003" を返します。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-144">Returns "1 January 2003".</span></span> <span data-ttu-id="3e1cb-145">テキスト検索では大文字と小文字が区別されるため、変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="3e1cb-145">No change is made because the text search is case-sensitive.</span></span> 
  

