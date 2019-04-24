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
description: 式の結果を formatpicture に従って書式設定された文字列として返します。
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339894"
---
# <a name="format-function"></a><span data-ttu-id="b6da9-103">FORMAT 関数</span><span class="sxs-lookup"><span data-stu-id="b6da9-103">FORMAT Function</span></span>

<span data-ttu-id="b6da9-104">_式_の結果を_formatpicture_に従って書式設定された文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="b6da9-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b6da9-105">構文</span><span class="sxs-lookup"><span data-stu-id="b6da9-105">Syntax</span></span>

<span data-ttu-id="b6da9-106">FORMAT (\* **式** *、"* \* *formatpicture* \* \*")</span><span class="sxs-lookup"><span data-stu-id="b6da9-106">FORMAT(\*\* *expression* \*\*," \*\* *formatpicture* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b6da9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6da9-107">Parameters</span></span>

|<span data-ttu-id="b6da9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="b6da9-108">**Name**</span></span>|<span data-ttu-id="b6da9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b6da9-109">**Required/Optional**</span></span>|<span data-ttu-id="b6da9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b6da9-110">**Data Type**</span></span>|<span data-ttu-id="b6da9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b6da9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b6da9-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="b6da9-112">_expression_</span></span> <br/> |<span data-ttu-id="b6da9-113">必須</span><span class="sxs-lookup"><span data-stu-id="b6da9-113">Required</span></span>  <br/> |<span data-ttu-id="b6da9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b6da9-114">**String**</span></span> <br/> |<span data-ttu-id="b6da9-115">定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。</span><span class="sxs-lookup"><span data-stu-id="b6da9-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="b6da9-116">_formatpicture_</span><span class="sxs-lookup"><span data-stu-id="b6da9-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="b6da9-117">必須</span><span class="sxs-lookup"><span data-stu-id="b6da9-117">Required</span></span>  <br/> |<span data-ttu-id="b6da9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b6da9-118">**String**</span></span> <br/> |<span data-ttu-id="b6da9-119">文字列を書式設定するための書式形式です。</span><span class="sxs-lookup"><span data-stu-id="b6da9-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b6da9-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="b6da9-120">Return value</span></span>

<span data-ttu-id="b6da9-121">文字列</span><span class="sxs-lookup"><span data-stu-id="b6da9-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6da9-122">注釈</span><span class="sxs-lookup"><span data-stu-id="b6da9-122">Remarks</span></span>

<span data-ttu-id="b6da9-123">式の種類および書式形式で指定されている形式に応じて、返される文字列の書式が決まります。</span><span class="sxs-lookup"><span data-stu-id="b6da9-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="b6da9-124">_formatpicture_は、式の種類に適している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6da9-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="b6da9-125">書式設定画像の指定の詳細については、「 [format pictures](about-format-pictures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6da9-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="b6da9-126">_式_の結果と_formatpicture_で想定される種類が異なる場合、または_formatpicture_に構文エラーがある場合は、エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="b6da9-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="b6da9-127">例 1</span><span class="sxs-lookup"><span data-stu-id="b6da9-127">Example 1</span></span>

<span data-ttu-id="b6da9-128">FORMAT(1cm/4, "0.000 u")</span><span class="sxs-lookup"><span data-stu-id="b6da9-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="b6da9-129">"0.250 cm" を返します。</span><span class="sxs-lookup"><span data-stu-id="b6da9-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b6da9-130">例 2</span><span class="sxs-lookup"><span data-stu-id="b6da9-130">Example 2</span></span>

<span data-ttu-id="b6da9-131">FORMAT(1cm/4, "0.00 U")</span><span class="sxs-lookup"><span data-stu-id="b6da9-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="b6da9-132">"0.25 CM" を返します。</span><span class="sxs-lookup"><span data-stu-id="b6da9-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b6da9-133">例 3</span><span class="sxs-lookup"><span data-stu-id="b6da9-133">Example 3</span></span>

<span data-ttu-id="b6da9-134">FORMAT(1cm/4, "0.0 u")</span><span class="sxs-lookup"><span data-stu-id="b6da9-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="b6da9-135">"0.3 cm" を返します。</span><span class="sxs-lookup"><span data-stu-id="b6da9-135">Returns "0.3 cm."</span></span>
  

