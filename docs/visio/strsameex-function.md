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
# <a name="strsameex-function"></a><span data-ttu-id="0c2b2-103">STRSAMEEX 関数</span><span class="sxs-lookup"><span data-stu-id="0c2b2-103">STRSAMEEX Function</span></span>

<span data-ttu-id="0c2b2-104">2 つの文字列が同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0c2b2-105">構文</span><span class="sxs-lookup"><span data-stu-id="0c2b2-105">Syntax</span></span>

<span data-ttu-id="0c2b2-106">場合は、STRSAMEEX ("* * *string1* * *「,」* **文字列 2* * *」、* **ロケール Id* * *、* **フラグ** *)</span><span class="sxs-lookup"><span data-stu-id="0c2b2-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0c2b2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c2b2-107">Parameters</span></span>

|<span data-ttu-id="0c2b2-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-108">**Name**</span></span>|<span data-ttu-id="0c2b2-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-109">**Required/Optional**</span></span>|<span data-ttu-id="0c2b2-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-110">**Data Type**</span></span>|<span data-ttu-id="0c2b2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0c2b2-112">_文字列 1_</span><span class="sxs-lookup"><span data-stu-id="0c2b2-112">_string1_</span></span> <br/> |<span data-ttu-id="0c2b2-113">必須</span><span class="sxs-lookup"><span data-stu-id="0c2b2-113">Required</span></span>  <br/> |<span data-ttu-id="0c2b2-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-114">**String**</span></span> <br/> |<span data-ttu-id="0c2b2-115">比較する最初の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="0c2b2-116">_文字列 2_</span><span class="sxs-lookup"><span data-stu-id="0c2b2-116">_string2_</span></span> <br/> |<span data-ttu-id="0c2b2-117">必須</span><span class="sxs-lookup"><span data-stu-id="0c2b2-117">Required</span></span>  <br/> |<span data-ttu-id="0c2b2-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-118">**String**</span></span> <br/> | <span data-ttu-id="0c2b2-119">比較する 2 番目の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="0c2b2-120">_ロケール Id_</span><span class="sxs-lookup"><span data-stu-id="0c2b2-120">_localeID_</span></span> <br/> |<span data-ttu-id="0c2b2-121">必須</span><span class="sxs-lookup"><span data-stu-id="0c2b2-121">Required</span></span>  <br/> |<span data-ttu-id="0c2b2-122">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-122">**Numeric**</span></span> <br/> |<span data-ttu-id="0c2b2-123">ロケールの ID を示すコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="0c2b2-124">_フラグ_</span><span class="sxs-lookup"><span data-stu-id="0c2b2-124">_flag_</span></span> <br/> |<span data-ttu-id="0c2b2-125">必須</span><span class="sxs-lookup"><span data-stu-id="0c2b2-125">Required</span></span>  <br/> |<span data-ttu-id="0c2b2-126">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-126">**Numeric**</span></span> <br/> | <span data-ttu-id="0c2b2-127">比較の種類を示すビットを指定します。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0c2b2-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="0c2b2-128">Return value</span></span>

<span data-ttu-id="0c2b2-129">ブール型</span><span class="sxs-lookup"><span data-stu-id="0c2b2-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c2b2-130">注釈</span><span class="sxs-lookup"><span data-stu-id="0c2b2-130">Remarks</span></span>

<span data-ttu-id="0c2b2-p101">STRSAMEEX は、2 つの入力文字列が同じ場合は TRUE を、異なる場合は FALSE を返します。マルチバイト文字列の比較、または特定のロケールに関する文字の規則を使用した比較を実行する場合に、この関数を使用します。
			
</span><span class="sxs-lookup"><span data-stu-id="0c2b2-p101">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't. Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="0c2b2-133">STRSAMEEX 関数では、次のフラグを任意に組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="0c2b2-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-134">**Flag**</span></span>|<span data-ttu-id="0c2b2-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="0c2b2-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c2b2-136">1</span><span class="sxs-lookup"><span data-stu-id="0c2b2-136">1</span></span>  <br/> |<span data-ttu-id="0c2b2-137">大文字/小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="0c2b2-138">2</span><span class="sxs-lookup"><span data-stu-id="0c2b2-138">2</span></span>  <br/> |<span data-ttu-id="0c2b2-139">間隔のない文字を無視します。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="0c2b2-140">4</span><span class="sxs-lookup"><span data-stu-id="0c2b2-140">4</span></span>  <br/> |<span data-ttu-id="0c2b2-141">記号を無視します。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="0c2b2-142">4096</span><span class="sxs-lookup"><span data-stu-id="0c2b2-142">4096</span></span>  <br/> |<span data-ttu-id="0c2b2-143">句読点を記号として扱います。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="0c2b2-144">65536</span><span class="sxs-lookup"><span data-stu-id="0c2b2-144">65536</span></span>  <br/> |<span data-ttu-id="0c2b2-145">ひらがなとカタカナを区別しません。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="0c2b2-146">131072</span><span class="sxs-lookup"><span data-stu-id="0c2b2-146">131072</span></span>  <br/> |<span data-ttu-id="0c2b2-147">半角文字 (1 バイト) と同じ文字の全角文字 (2 バイト) を区別しません。</span><span class="sxs-lookup"><span data-stu-id="0c2b2-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

