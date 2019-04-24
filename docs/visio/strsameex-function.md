---
title: STRSAMEEX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: 2つの文字列が同じかどうかを判断します。
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329793"
---
# <a name="strsameex-function"></a><span data-ttu-id="90150-103">STRSAMEEX 関数</span><span class="sxs-lookup"><span data-stu-id="90150-103">STRSAMEEX Function</span></span>

<span data-ttu-id="90150-104">2つの文字列が同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="90150-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="90150-105">構文</span><span class="sxs-lookup"><span data-stu-id="90150-105">Syntax</span></span>

<span data-ttu-id="90150-106">strsameex ("\* \* *string1* \* *", "* \* *string2* \* \*", \* \* *localeID* \* \*, \* \* *flag* \* \*)</span><span class="sxs-lookup"><span data-stu-id="90150-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="90150-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90150-107">Parameters</span></span>

|<span data-ttu-id="90150-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="90150-108">**Name**</span></span>|<span data-ttu-id="90150-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="90150-109">**Required/Optional**</span></span>|<span data-ttu-id="90150-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="90150-110">**Data Type**</span></span>|<span data-ttu-id="90150-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="90150-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="90150-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="90150-112">_string1_</span></span> <br/> |<span data-ttu-id="90150-113">必須</span><span class="sxs-lookup"><span data-stu-id="90150-113">Required</span></span>  <br/> |<span data-ttu-id="90150-114">**String**</span><span class="sxs-lookup"><span data-stu-id="90150-114">**String**</span></span> <br/> |<span data-ttu-id="90150-115">比較する最初の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="90150-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="90150-116">_string2_</span><span class="sxs-lookup"><span data-stu-id="90150-116">_string2_</span></span> <br/> |<span data-ttu-id="90150-117">必須</span><span class="sxs-lookup"><span data-stu-id="90150-117">Required</span></span>  <br/> |<span data-ttu-id="90150-118">**String**</span><span class="sxs-lookup"><span data-stu-id="90150-118">**String**</span></span> <br/> | <span data-ttu-id="90150-119">比較する 2 番目の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="90150-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="90150-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="90150-120">_localeID_</span></span> <br/> |<span data-ttu-id="90150-121">必須</span><span class="sxs-lookup"><span data-stu-id="90150-121">Required</span></span>  <br/> |<span data-ttu-id="90150-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="90150-122">**Numeric**</span></span> <br/> |<span data-ttu-id="90150-123">ロケールの ID を示すコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="90150-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="90150-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="90150-124">_flag_</span></span> <br/> |<span data-ttu-id="90150-125">必須</span><span class="sxs-lookup"><span data-stu-id="90150-125">Required</span></span>  <br/> |<span data-ttu-id="90150-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="90150-126">**Numeric**</span></span> <br/> | <span data-ttu-id="90150-127">比較の種類を示すビットを指定します。</span><span class="sxs-lookup"><span data-stu-id="90150-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="90150-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="90150-128">Return value</span></span>

<span data-ttu-id="90150-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="90150-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90150-130">解説</span><span class="sxs-lookup"><span data-stu-id="90150-130">Remarks</span></span>

<span data-ttu-id="90150-131">STRSAMEEX は、2 つの入力文字列が同じ場合は TRUE を、異なる場合は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="90150-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="90150-132">マルチバイト文字列の比較、または特定のロケールに関する文字の規則を使用した比較を実行する場合に、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="90150-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="90150-133">STRSAMEEX 関数では、次のフラグを任意に組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="90150-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="90150-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="90150-134">**Flag**</span></span>|<span data-ttu-id="90150-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="90150-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90150-136">1-d</span><span class="sxs-lookup"><span data-stu-id="90150-136">1</span></span>  <br/> |<span data-ttu-id="90150-137">大文字/小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="90150-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="90150-138">pbm-2</span><span class="sxs-lookup"><span data-stu-id="90150-138">2</span></span>  <br/> |<span data-ttu-id="90150-139">間隔のない文字を無視します。</span><span class="sxs-lookup"><span data-stu-id="90150-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="90150-140">2/4</span><span class="sxs-lookup"><span data-stu-id="90150-140">4</span></span>  <br/> |<span data-ttu-id="90150-141">記号を無視します。</span><span class="sxs-lookup"><span data-stu-id="90150-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="90150-142">4096</span><span class="sxs-lookup"><span data-stu-id="90150-142">4096</span></span>  <br/> |<span data-ttu-id="90150-143">句読点を記号として扱います。</span><span class="sxs-lookup"><span data-stu-id="90150-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="90150-144">65536</span><span class="sxs-lookup"><span data-stu-id="90150-144">65536</span></span>  <br/> |<span data-ttu-id="90150-145">ひらがなとカタカナを区別しません。</span><span class="sxs-lookup"><span data-stu-id="90150-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="90150-146">131072</span><span class="sxs-lookup"><span data-stu-id="90150-146">131072</span></span>  <br/> |<span data-ttu-id="90150-147">半角文字 (1 バイト) と同じ文字の全角文字 (2 バイト) を区別しません。</span><span class="sxs-lookup"><span data-stu-id="90150-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

