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
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806373"
---
# <a name="setf-function"></a><span data-ttu-id="89e59-103">SETF 関数</span><span class="sxs-lookup"><span data-stu-id="89e59-103">SETF Function</span></span>

<span data-ttu-id="89e59-104">セルの数式を設定します。</span><span class="sxs-lookup"><span data-stu-id="89e59-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="89e59-105">構文</span><span class="sxs-lookup"><span data-stu-id="89e59-105">Syntax</span></span>

<span data-ttu-id="89e59-106">SETF (GETREF (* **セル** *)、* **式** *)</span><span class="sxs-lookup"><span data-stu-id="89e59-106">SETF( GETREF(** *cell* ** ), ** *formula* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="89e59-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89e59-107">Parameters</span></span>

|<span data-ttu-id="89e59-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="89e59-108">**Name**</span></span>|<span data-ttu-id="89e59-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="89e59-109">**Required/Optional**</span></span>|<span data-ttu-id="89e59-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="89e59-110">**Data Type**</span></span>|<span data-ttu-id="89e59-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="89e59-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="89e59-112">_セル_</span><span class="sxs-lookup"><span data-stu-id="89e59-112">_cell_</span></span> <br/> |<span data-ttu-id="89e59-113">必須</span><span class="sxs-lookup"><span data-stu-id="89e59-113">Required</span></span>  <br/> |<span data-ttu-id="89e59-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="89e59-114">**String**</span></span> <br/> |<span data-ttu-id="89e59-115">セルの数式を設定するのには。</span><span class="sxs-lookup"><span data-stu-id="89e59-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="89e59-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="89e59-116">_formula_</span></span> <br/> |<span data-ttu-id="89e59-117">必須</span><span class="sxs-lookup"><span data-stu-id="89e59-117">Required</span></span>  <br/> |<span data-ttu-id="89e59-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="89e59-118">**String**</span></span> <br/> |<span data-ttu-id="89e59-119">使用する数式を指定します。</span><span class="sxs-lookup"><span data-stu-id="89e59-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89e59-120">注釈</span><span class="sxs-lookup"><span data-stu-id="89e59-120">Remarks</span></span>

<span data-ttu-id="89e59-121">評価するときは、_セル_に新しい数式が_数式_内の式の結果になります。</span><span class="sxs-lookup"><span data-stu-id="89e59-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="89e59-122">_数式_は、引用符で囲まれたが、引用符で囲まれた式が_セル_に書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="89e59-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="89e59-123">_セル_を文字列に設定するには、3 つの引用符 () で_数式_を囲みます。</span><span class="sxs-lookup"><span data-stu-id="89e59-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="89e59-p102">循環処理を避けるために、ターゲット セルは、GETREF() による参照を使用して指定するか、または文字列として指定する必要があります。Microsoft Visio では、図形を別の図面に移動したときに参照が調整されるので、GETREF を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="89e59-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="89e59-126">_セル_が GETREF を使用して指定されていない場合、または文字列として、関数には、エラーが返され、ないセルの数式を変更します。</span><span class="sxs-lookup"><span data-stu-id="89e59-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="89e59-127">_数式_に構文エラーが含まれている場合、関数はエラーを返し、_セル_の数式は変更されません。</span><span class="sxs-lookup"><span data-stu-id="89e59-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="89e59-128">例 1</span><span class="sxs-lookup"><span data-stu-id="89e59-128">Example 1</span></span>

<span data-ttu-id="89e59-129">SETF (GETREF(Scratch.A1)、1.5 で\*6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="89e59-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="89e59-130">Scratch.A1 の数式を 21 インチに設定します。</span><span class="sxs-lookup"><span data-stu-id="89e59-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="89e59-131">例 2</span><span class="sxs-lookup"><span data-stu-id="89e59-131">Example 2</span></span>

<span data-ttu-id="89e59-132">SETF (GETREF(Scratch.A1)、"の 1.5 \* 6 + 1 フィート」)</span><span class="sxs-lookup"><span data-stu-id="89e59-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="89e59-133">最初の数式を設定します。</span><span class="sxs-lookup"><span data-stu-id="89e59-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="89e59-134">A1 に、式 1.5\*6 + 1 フィートです。</span><span class="sxs-lookup"><span data-stu-id="89e59-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="89e59-135">例 3</span><span class="sxs-lookup"><span data-stu-id="89e59-135">Example 3</span></span>

<span data-ttu-id="89e59-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="89e59-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="89e59-137">Scratch.A1 の数式を、文字列 "Say ""ahh""" に設定します。これは "Say "ahh"" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="89e59-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

