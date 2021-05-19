---
title: SETF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: セルの数式を設定します。
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425975"
---
# <a name="setf-function"></a><span data-ttu-id="cb64c-103">SETF 関数</span><span class="sxs-lookup"><span data-stu-id="cb64c-103">SETF Function</span></span>

<span data-ttu-id="cb64c-104">セルの数式を設定します。</span><span class="sxs-lookup"><span data-stu-id="cb64c-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cb64c-105">構文</span><span class="sxs-lookup"><span data-stu-id="cb64c-105">Syntax</span></span>

<span data-ttu-id="cb64c-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span><span class="sxs-lookup"><span data-stu-id="cb64c-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cb64c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cb64c-107">Parameters</span></span>

|<span data-ttu-id="cb64c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="cb64c-108">**Name**</span></span>|<span data-ttu-id="cb64c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="cb64c-109">**Required/Optional**</span></span>|<span data-ttu-id="cb64c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="cb64c-110">**Data Type**</span></span>|<span data-ttu-id="cb64c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb64c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cb64c-112">_セル_</span><span class="sxs-lookup"><span data-stu-id="cb64c-112">_cell_</span></span> <br/> |<span data-ttu-id="cb64c-113">必須</span><span class="sxs-lookup"><span data-stu-id="cb64c-113">Required</span></span>  <br/> |<span data-ttu-id="cb64c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="cb64c-114">**String**</span></span> <br/> |<span data-ttu-id="cb64c-115">数式を設定するセル。</span><span class="sxs-lookup"><span data-stu-id="cb64c-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="cb64c-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="cb64c-116">_formula_</span></span> <br/> |<span data-ttu-id="cb64c-117">必須</span><span class="sxs-lookup"><span data-stu-id="cb64c-117">Required</span></span>  <br/> |<span data-ttu-id="cb64c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="cb64c-118">**String**</span></span> <br/> |<span data-ttu-id="cb64c-119">使用する数式を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb64c-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb64c-120">注釈</span><span class="sxs-lookup"><span data-stu-id="cb64c-120">Remarks</span></span>

<span data-ttu-id="cb64c-121">評価すると、数式の式の結果  _がセルの_ 新しい数式  _になります_。</span><span class="sxs-lookup"><span data-stu-id="cb64c-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="cb64c-122">数式  _を_ 二重引用符で囲む場合、引用符で囲まれた式はセルに書き込  _まれます_。</span><span class="sxs-lookup"><span data-stu-id="cb64c-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="cb64c-123">セルを  _文字列に_ 設定するには、  _数式を_ 3 つの二重引用符で囲みます。</span><span class="sxs-lookup"><span data-stu-id="cb64c-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="cb64c-p102">循環処理を避けるために、ターゲット セルは、GETREF() による参照を使用して指定するか、または文字列として指定する必要があります。Microsoft Visio では、図形を別の図面に移動したときに参照が調整されるので、GETREF を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cb64c-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="cb64c-126">GETREF  _または_ 文字列を使用してセルを指定しない場合、関数はエラーを返し、セルの数式は変更されません。</span><span class="sxs-lookup"><span data-stu-id="cb64c-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="cb64c-127">数式  _に_ 構文エラーが含まれている場合、関数はエラーを返し、セル内の数式  _は_ 変更されません。</span><span class="sxs-lookup"><span data-stu-id="cb64c-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cb64c-128">例 1</span><span class="sxs-lookup"><span data-stu-id="cb64c-128">Example 1</span></span>

<span data-ttu-id="cb64c-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="cb64c-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="cb64c-130">Scratch.A1 の数式を 21 インチに設定します。</span><span class="sxs-lookup"><span data-stu-id="cb64c-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cb64c-131">例 2</span><span class="sxs-lookup"><span data-stu-id="cb64c-131">Example 2</span></span>

<span data-ttu-id="cb64c-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span><span class="sxs-lookup"><span data-stu-id="cb64c-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="cb64c-133">Scratch の数式を設定します。</span><span class="sxs-lookup"><span data-stu-id="cb64c-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="cb64c-134">A1 ~ 6+1 \* ft の式 1.5。</span><span class="sxs-lookup"><span data-stu-id="cb64c-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="cb64c-135">例 3</span><span class="sxs-lookup"><span data-stu-id="cb64c-135">Example 3</span></span>

<span data-ttu-id="cb64c-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="cb64c-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="cb64c-137">Scratch.A1 の数式を、文字列 "Say ""ahh""" に設定します。これは "Say "ahh"" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb64c-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

