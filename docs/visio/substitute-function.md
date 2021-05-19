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
description: テキスト文字列の一部を別のテキスト文字列に置き換える。
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346824"
---
# <a name="substitute-function"></a><span data-ttu-id="dc7c9-103">SUBSTITUTE 関数</span><span class="sxs-lookup"><span data-stu-id="dc7c9-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="dc7c9-104">テキスト文字列の一部を別のテキスト文字列に置き換える。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dc7c9-105">構文</span><span class="sxs-lookup"><span data-stu-id="dc7c9-105">Syntax</span></span>

 <span data-ttu-id="dc7c9-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\*\*\* new_text \*\* [, \*\*\*\* start_num \*\* \*\*, \*\*\*\* ignore_case_opt \*\* )</span><span class="sxs-lookup"><span data-stu-id="dc7c9-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dc7c9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dc7c9-107">Parameters</span></span>

|<span data-ttu-id="dc7c9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-108">**Name**</span></span>|<span data-ttu-id="dc7c9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-109">**Required/Optional**</span></span>|<span data-ttu-id="dc7c9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-110">**Data Type**</span></span>|<span data-ttu-id="dc7c9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dc7c9-112">_text_</span><span class="sxs-lookup"><span data-stu-id="dc7c9-112">_text_</span></span> <br/> |<span data-ttu-id="dc7c9-113">必須</span><span class="sxs-lookup"><span data-stu-id="dc7c9-113">Required</span></span>  <br/> |<span data-ttu-id="dc7c9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-114">**String**</span></span> <br/> | <span data-ttu-id="dc7c9-115">文字を置き換えるテキストを含むセルへのテキストまたは参照。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="dc7c9-116">_old_text_</span><span class="sxs-lookup"><span data-stu-id="dc7c9-116">_old_text_</span></span> <br/> |<span data-ttu-id="dc7c9-117">必須</span><span class="sxs-lookup"><span data-stu-id="dc7c9-117">Required</span></span>  <br/> |<span data-ttu-id="dc7c9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-118">**String**</span></span> <br/> | <span data-ttu-id="dc7c9-119">置換するテキスト。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="dc7c9-120">_new_text_</span><span class="sxs-lookup"><span data-stu-id="dc7c9-120">_new_text_</span></span> <br/> |<span data-ttu-id="dc7c9-121">必須</span><span class="sxs-lookup"><span data-stu-id="dc7c9-121">Required</span></span>  <br/> |<span data-ttu-id="dc7c9-122">**String**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-122">**String**</span></span> <br/> | <span data-ttu-id="dc7c9-123">文字列を置換するために使用 _するold_text。_</span><span class="sxs-lookup"><span data-stu-id="dc7c9-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="dc7c9-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="dc7c9-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="dc7c9-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="dc7c9-125">Optional</span></span>  <br/> |<span data-ttu-id="dc7c9-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-126">**Numeric**</span></span> <br/> |<span data-ttu-id="dc7c9-127">置換するファイルのold_text指定します。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="dc7c9-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="dc7c9-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="dc7c9-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="dc7c9-129">Optional</span></span>  <br/> |<span data-ttu-id="dc7c9-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc7c9-130">**Boolean**</span></span> <br/> |<span data-ttu-id="dc7c9-131">大文字と小文字を区別する場合は FALSE。それ以外の場合は TRUE。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="dc7c9-132">既定値は "FALSE" です。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dc7c9-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="dc7c9-133">Return value</span></span>

<span data-ttu-id="dc7c9-134">文字列</span><span class="sxs-lookup"><span data-stu-id="dc7c9-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc7c9-135">注釈</span><span class="sxs-lookup"><span data-stu-id="dc7c9-135">Remarks</span></span>

 <span data-ttu-id="dc7c9-136">この値を  _指定start_num_opt、_ その  _出現回数old_text_ 置き換えられる。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="dc7c9-137">それ以外の場合は、_テキストold_text__の出現_ 回数が 1 回 _にnew_text。_</span><span class="sxs-lookup"><span data-stu-id="dc7c9-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="dc7c9-138">テキスト文字列内の特定のテキストを置き換える場合は、SUBSTITUTE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="dc7c9-139">テキスト文字列内の特定の場所で発生するテキストを置き換える場合は、REPLACE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="dc7c9-140">例</span><span class="sxs-lookup"><span data-stu-id="dc7c9-140">Example</span></span>

<span data-ttu-id="dc7c9-141">SUBSTITUTE ("2003 年 1 月 1 日"、"1 月"、"JAN")</span><span class="sxs-lookup"><span data-stu-id="dc7c9-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="dc7c9-142">"1 JAN 2003" を返します。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="dc7c9-143">SUBSTITUTE ("2003 年 1 月 1 日","1 月","JAN")</span><span class="sxs-lookup"><span data-stu-id="dc7c9-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="dc7c9-144">"2003 年 1 月 1 日" を返します。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-144">Returns "1 January 2003".</span></span> <span data-ttu-id="dc7c9-145">テキスト検索では大文字と小文字が区別されるので、変更は行なされません。</span><span class="sxs-lookup"><span data-stu-id="dc7c9-145">No change is made because the text search is case-sensitive.</span></span> 
  

