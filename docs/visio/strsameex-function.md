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
description: 2 つの文字列が同じかどうかを判断します。
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806589"
---
# <a name="strsameex-function"></a><span data-ttu-id="981b9-103">STRSAMEEX 関数</span><span class="sxs-lookup"><span data-stu-id="981b9-103">STRSAMEEX Function</span></span>

<span data-ttu-id="981b9-104">2 つの文字列が同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="981b9-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="981b9-105">構文</span><span class="sxs-lookup"><span data-stu-id="981b9-105">Syntax</span></span>

<span data-ttu-id="981b9-106">場合は、STRSAMEEX ("* * *string1* * *「,」* **文字列 2* * *」、* **ロケール Id* * *、* **フラグ** *)</span><span class="sxs-lookup"><span data-stu-id="981b9-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="981b9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="981b9-107">Parameters</span></span>

|<span data-ttu-id="981b9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="981b9-108">**Name**</span></span>|<span data-ttu-id="981b9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="981b9-109">**Required/Optional**</span></span>|<span data-ttu-id="981b9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="981b9-110">**Data Type**</span></span>|<span data-ttu-id="981b9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="981b9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="981b9-112">_文字列 1_</span><span class="sxs-lookup"><span data-stu-id="981b9-112">_string1_</span></span> <br/> |<span data-ttu-id="981b9-113">必須</span><span class="sxs-lookup"><span data-stu-id="981b9-113">Required</span></span>  <br/> |<span data-ttu-id="981b9-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="981b9-114">**String**</span></span> <br/> |<span data-ttu-id="981b9-115">比較する最初の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="981b9-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="981b9-116">_文字列 2_</span><span class="sxs-lookup"><span data-stu-id="981b9-116">_string2_</span></span> <br/> |<span data-ttu-id="981b9-117">必須</span><span class="sxs-lookup"><span data-stu-id="981b9-117">Required</span></span>  <br/> |<span data-ttu-id="981b9-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="981b9-118">**String**</span></span> <br/> | <span data-ttu-id="981b9-119">比較する 2 番目の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="981b9-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="981b9-120">_ロケール Id_</span><span class="sxs-lookup"><span data-stu-id="981b9-120">_localeID_</span></span> <br/> |<span data-ttu-id="981b9-121">必須</span><span class="sxs-lookup"><span data-stu-id="981b9-121">Required</span></span>  <br/> |<span data-ttu-id="981b9-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="981b9-122">**Numeric**</span></span> <br/> |<span data-ttu-id="981b9-123">ロケールの ID を示すコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="981b9-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="981b9-124">_フラグ_</span><span class="sxs-lookup"><span data-stu-id="981b9-124">_flag_</span></span> <br/> |<span data-ttu-id="981b9-125">必須</span><span class="sxs-lookup"><span data-stu-id="981b9-125">Required</span></span>  <br/> |<span data-ttu-id="981b9-126">**数値**</span><span class="sxs-lookup"><span data-stu-id="981b9-126">**Numeric**</span></span> <br/> | <span data-ttu-id="981b9-127">比較の種類を示すビットを指定します。</span><span class="sxs-lookup"><span data-stu-id="981b9-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="981b9-128">�߂�l</span><span class="sxs-lookup"><span data-stu-id="981b9-128">Return value</span></span>

<span data-ttu-id="981b9-129">ブール型</span><span class="sxs-lookup"><span data-stu-id="981b9-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="981b9-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="981b9-130">Remarks</span></span>

<span data-ttu-id="981b9-131">両方の入力文字列が同じ場合は TRUE と FALSE を指定するとされていない場合は、STRSAMEEX を返します。</span><span class="sxs-lookup"><span data-stu-id="981b9-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="981b9-132">マルチバイト文字列を比較する、または特定のロケールの規則を使用する比較を行うには、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="981b9-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="981b9-133">STRSAMEEX 関数では、次のフラグを任意に組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="981b9-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="981b9-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="981b9-134">**Flag**</span></span>|<span data-ttu-id="981b9-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="981b9-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="981b9-136">1</span><span class="sxs-lookup"><span data-stu-id="981b9-136">1</span></span>  <br/> |<span data-ttu-id="981b9-137">大文字/小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="981b9-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="981b9-138">2</span><span class="sxs-lookup"><span data-stu-id="981b9-138">2</span></span>  <br/> |<span data-ttu-id="981b9-139">間隔のない文字を無視します。</span><span class="sxs-lookup"><span data-stu-id="981b9-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="981b9-140">4</span><span class="sxs-lookup"><span data-stu-id="981b9-140">4</span></span>  <br/> |<span data-ttu-id="981b9-141">記号を無視します。</span><span class="sxs-lookup"><span data-stu-id="981b9-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="981b9-142">4096</span><span class="sxs-lookup"><span data-stu-id="981b9-142">4096</span></span>  <br/> |<span data-ttu-id="981b9-143">句読点を記号として扱います。</span><span class="sxs-lookup"><span data-stu-id="981b9-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="981b9-144">65536</span><span class="sxs-lookup"><span data-stu-id="981b9-144">65536</span></span>  <br/> |<span data-ttu-id="981b9-145">ひらがなとカタカナを区別しません。</span><span class="sxs-lookup"><span data-stu-id="981b9-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="981b9-146">131072</span><span class="sxs-lookup"><span data-stu-id="981b9-146">131072</span></span>  <br/> |<span data-ttu-id="981b9-147">半角文字 (1 バイト) と同じ文字の全角文字 (2 バイト) を区別しません。</span><span class="sxs-lookup"><span data-stu-id="981b9-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

