---
title: FORMAT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Formatpicture に従って書式設定された文字列としての式の結果を返します。
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805444"
---
# <a name="format-function"></a><span data-ttu-id="e9354-103">FORMAT 関数</span><span class="sxs-lookup"><span data-stu-id="e9354-103">FORMAT Function</span></span>

<span data-ttu-id="e9354-104">_Formatpicture_に従って書式設定された文字列としての_式_の結果を返します。</span><span class="sxs-lookup"><span data-stu-id="e9354-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e9354-105">構文</span><span class="sxs-lookup"><span data-stu-id="e9354-105">Syntax</span></span>

<span data-ttu-id="e9354-106">形式 (* **式** *、"* * *formatpicture* * *")</span><span class="sxs-lookup"><span data-stu-id="e9354-106">FORMAT(** *expression* **," ** *formatpicture* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e9354-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e9354-107">Parameters</span></span>

|<span data-ttu-id="e9354-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="e9354-108">**Name**</span></span>|<span data-ttu-id="e9354-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e9354-109">**Required/Optional**</span></span>|<span data-ttu-id="e9354-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e9354-110">**Data Type**</span></span>|<span data-ttu-id="e9354-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e9354-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e9354-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="e9354-112">_expression_</span></span> <br/> |<span data-ttu-id="e9354-113">必須</span><span class="sxs-lookup"><span data-stu-id="e9354-113">Required</span></span>  <br/> |<span data-ttu-id="e9354-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="e9354-114">**String**</span></span> <br/> |<span data-ttu-id="e9354-115">定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。</span><span class="sxs-lookup"><span data-stu-id="e9354-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="e9354-116">_formatpicture_</span><span class="sxs-lookup"><span data-stu-id="e9354-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="e9354-117">必須</span><span class="sxs-lookup"><span data-stu-id="e9354-117">Required</span></span>  <br/> |<span data-ttu-id="e9354-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="e9354-118">**String**</span></span> <br/> |<span data-ttu-id="e9354-119">文字列を書式設定するための書式形式です。</span><span class="sxs-lookup"><span data-stu-id="e9354-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e9354-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e9354-120">Return value</span></span>

<span data-ttu-id="e9354-121">String</span><span class="sxs-lookup"><span data-stu-id="e9354-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9354-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="e9354-122">Remarks</span></span>

<span data-ttu-id="e9354-123">式の型と、図の書式設定で指定された型は、返される文字列の動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="e9354-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="e9354-124">_Formatpicture_は、式のタイプに対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9354-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="e9354-125">書式形式を指定する方法の詳細については、[書式形式について](about-format-pictures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9354-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="e9354-126">_式_と_formatpicture_での型の結果は、異なる種類の場合、または_formatpicture_で構文エラーがある場合は、エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="e9354-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="e9354-127">例 1</span><span class="sxs-lookup"><span data-stu-id="e9354-127">Example 1</span></span>

<span data-ttu-id="e9354-128">FORMAT(1cm/4, "0.000 u")</span><span class="sxs-lookup"><span data-stu-id="e9354-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="e9354-129">"0.250 cm" を返します。</span><span class="sxs-lookup"><span data-stu-id="e9354-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e9354-130">例 2</span><span class="sxs-lookup"><span data-stu-id="e9354-130">Example 2</span></span>

<span data-ttu-id="e9354-131">FORMAT(1cm/4, "0.00 U")</span><span class="sxs-lookup"><span data-stu-id="e9354-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="e9354-132">"0.25 CM" を返します。</span><span class="sxs-lookup"><span data-stu-id="e9354-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e9354-133">例 3</span><span class="sxs-lookup"><span data-stu-id="e9354-133">Example 3</span></span>

<span data-ttu-id="e9354-134">FORMAT(1cm/4, "0.0 u")</span><span class="sxs-lookup"><span data-stu-id="e9354-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="e9354-135">"0.3 cm" を返します。</span><span class="sxs-lookup"><span data-stu-id="e9354-135">Returns "0.3 cm."</span></span>
  

