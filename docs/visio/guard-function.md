---
title: GUARD 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: 実行されるアクション、図面ウィンドウ、たとえば、移動、サイズ変更、グループ化、または図形のグループ化を解除して、削除、および変更から式を保護します。
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805493"
---
# <a name="guard-function"></a><span data-ttu-id="6a6ec-103">GUARD 関数</span><span class="sxs-lookup"><span data-stu-id="6a6ec-103">GUARD Function</span></span>

<span data-ttu-id="6a6ec-104">実行されるアクション、図面ウィンドウ、たとえば、移動、サイズ変更、グループ化、または図形のグループ化を解除して、削除、および変更から*式*を保護します。</span><span class="sxs-lookup"><span data-stu-id="6a6ec-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6a6ec-105">構文</span><span class="sxs-lookup"><span data-stu-id="6a6ec-105">Syntax</span></span>

<span data-ttu-id="6a6ec-106">ガード (* **式** *)</span><span class="sxs-lookup"><span data-stu-id="6a6ec-106">GUARD(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6a6ec-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a6ec-107">Parameters</span></span>

|<span data-ttu-id="6a6ec-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6a6ec-108">**Name**</span></span>|<span data-ttu-id="6a6ec-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6a6ec-109">**Required/Optional**</span></span>|<span data-ttu-id="6a6ec-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6a6ec-110">**Data Type**</span></span>|<span data-ttu-id="6a6ec-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6a6ec-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6a6ec-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="6a6ec-112">_expression_</span></span> <br/> |<span data-ttu-id="6a6ec-113">必須</span><span class="sxs-lookup"><span data-stu-id="6a6ec-113">Required</span></span>  <br/> |<span data-ttu-id="6a6ec-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6a6ec-114">**String**</span></span> <br/> |<span data-ttu-id="6a6ec-115">定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。</span><span class="sxs-lookup"><span data-stu-id="6a6ec-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a6ec-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6a6ec-116">Remarks</span></span>

<span data-ttu-id="6a6ec-117">GUARD 関数による影響を受ける主なセルは、[Width]、[Height]、[PinX]、[PinY] です。</span><span class="sxs-lookup"><span data-stu-id="6a6ec-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="6a6ec-p101">セルの数式を保護すると、図面ウィンドウでのアクションによってそのセルの値が変更されるのを防ぐことができます。ただし、図面ウィンドウで行う 1 つのアクションが複数のセルに影響することがあるため、図形の外観に予期しない変更が生じないようにするには、個々のセルを保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a6ec-p101">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window. However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6a6ec-120">例</span><span class="sxs-lookup"><span data-stu-id="6a6ec-120">Example</span></span>

<span data-ttu-id="6a6ec-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span><span class="sxs-lookup"><span data-stu-id="6a6ec-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="6a6ec-p102">図形の [Shape Transform] セクションの [Width] セルにこの式を設定すると、図面ウィンドウの図形の幅が変更されたときに式 (TEXTWIDTH(TheText) + 0.5 in) が別の値に置き換えられるのを防ぐことができます。TheText には関連する図形のテキストの構成が変更されたときにトリガーされるセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="6a6ec-p102">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window. TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

