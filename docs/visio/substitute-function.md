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
description: テキスト文字列の一部を別の文字列に置き換えます。
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643214"
---
# <a name="substitute-function"></a><span data-ttu-id="d744f-103">SUBSTITUTE 関数</span><span class="sxs-lookup"><span data-stu-id="d744f-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="d744f-104">テキスト文字列の一部を別の文字列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d744f-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d744f-105">構文</span><span class="sxs-lookup"><span data-stu-id="d744f-105">Syntax</span></span>

 <span data-ttu-id="d744f-106">代用 (\* **テキスト** *、* **文字列** *、* **と** \* [、\* **開始** *] [、* \* *ignore_case_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d744f-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d744f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d744f-107">Parameters</span></span>

|<span data-ttu-id="d744f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d744f-108">**Name**</span></span>|<span data-ttu-id="d744f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d744f-109">**Required/Optional**</span></span>|<span data-ttu-id="d744f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d744f-110">**Data Type**</span></span>|<span data-ttu-id="d744f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d744f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d744f-112">_text_</span><span class="sxs-lookup"><span data-stu-id="d744f-112">_text_</span></span> <br/> |<span data-ttu-id="d744f-113">必須</span><span class="sxs-lookup"><span data-stu-id="d744f-113">Required</span></span>  <br/> |<span data-ttu-id="d744f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d744f-114">**String**</span></span> <br/> | <span data-ttu-id="d744f-115">置換前の文字列を含む文字列、またはその文字列を含むセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="d744f-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="d744f-116">_文字列_</span><span class="sxs-lookup"><span data-stu-id="d744f-116">_old_text_</span></span> <br/> |<span data-ttu-id="d744f-117">必須</span><span class="sxs-lookup"><span data-stu-id="d744f-117">Required</span></span>  <br/> |<span data-ttu-id="d744f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d744f-118">**String**</span></span> <br/> | <span data-ttu-id="d744f-119">置換前の文字列を指定します。
</span><span class="sxs-lookup"><span data-stu-id="d744f-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="d744f-120">_置換_</span><span class="sxs-lookup"><span data-stu-id="d744f-120">_new_text_</span></span> <br/> |<span data-ttu-id="d744f-121">必須</span><span class="sxs-lookup"><span data-stu-id="d744f-121">Required</span></span>  <br/> |<span data-ttu-id="d744f-122">**String**</span><span class="sxs-lookup"><span data-stu-id="d744f-122">**String**</span></span> <br/> | <span data-ttu-id="d744f-123">_文字列_の置換に使用するテキストです。</span><span class="sxs-lookup"><span data-stu-id="d744f-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="d744f-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="d744f-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="d744f-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="d744f-125">Optional</span></span>  <br/> |<span data-ttu-id="d744f-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="d744f-126">**Numeric**</span></span> <br/> |<span data-ttu-id="d744f-127">置換する文字列の出現箇所を指定します。</span><span class="sxs-lookup"><span data-stu-id="d744f-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="d744f-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="d744f-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="d744f-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="d744f-129">Optional</span></span>  <br/> |<span data-ttu-id="d744f-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d744f-130">**Boolean**</span></span> <br/> |<span data-ttu-id="d744f-p101">大文字と小文字を区別する場合は FALSE、区別しない場合は TRUE です。既定値は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="d744f-p101">FALSE if case-sensitive; otherwise, TRUE. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d744f-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="d744f-133">Return value</span></span>

<span data-ttu-id="d744f-134">文字列</span><span class="sxs-lookup"><span data-stu-id="d744f-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d744f-135">注釈</span><span class="sxs-lookup"><span data-stu-id="d744f-135">Remarks</span></span>

 <span data-ttu-id="d744f-136">_Start_num_opt_を指定する場合のみ、検索_文字列_が置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d744f-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="d744f-137">_テキスト__文字列_に一致するすべてを変更する場合は、_置換します_。</span><span class="sxs-lookup"><span data-stu-id="d744f-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="d744f-138">テキスト文字列内の特定のテキストを置換する場合は、代替の関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="d744f-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="d744f-139">テキスト文字列内の特定の位置にある文字列を置換する場合は、REPLACE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="d744f-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="d744f-140">例</span><span class="sxs-lookup"><span data-stu-id="d744f-140">Example</span></span>

<span data-ttu-id="d744f-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span><span class="sxs-lookup"><span data-stu-id="d744f-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="d744f-142">"1 JAN 2003" を返します。</span><span class="sxs-lookup"><span data-stu-id="d744f-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="d744f-143">SUBSTITUTE ("1 January 2003","january","JAN")</span><span class="sxs-lookup"><span data-stu-id="d744f-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="d744f-144">「1 Jan 2003」を返します。</span><span class="sxs-lookup"><span data-stu-id="d744f-144">Returns "1 January 2003".</span></span> <span data-ttu-id="d744f-145">テキスト検索では大文字小文字を区別するため、変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="d744f-145">No change is made because the text search is case-sensitive.</span></span> 
  

