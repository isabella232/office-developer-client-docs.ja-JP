---
title: USE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: '[linepattern]、[fillpattern]、[beginarrow]、または [endarrow] セルに配置されたときに、name という名前の線パターン、塗りつぶしパターン、または線の端点を図形に適用します。'
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337150"
---
# <a name="use-function"></a><span data-ttu-id="d084b-103">USE 関数</span><span class="sxs-lookup"><span data-stu-id="d084b-103">USE Function</span></span>

<span data-ttu-id="d084b-104">[linepattern]、[fillpattern]、[beginarrow]、または [endarrow] セルに配置されたときに、name という_名前_の線パターン、塗りつぶしパターン、または線の端点を図形に適用します。</span><span class="sxs-lookup"><span data-stu-id="d084b-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d084b-105">構文</span><span class="sxs-lookup"><span data-stu-id="d084b-105">Syntax</span></span>

<span data-ttu-id="d084b-106">USE ("\* \* *name* \* \*")</span><span class="sxs-lookup"><span data-stu-id="d084b-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d084b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d084b-107">Parameters</span></span>

|<span data-ttu-id="d084b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d084b-108">**Name**</span></span>|<span data-ttu-id="d084b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d084b-109">**Required/Optional**</span></span>|<span data-ttu-id="d084b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d084b-110">**Data Type**</span></span>|<span data-ttu-id="d084b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d084b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d084b-112">_name_</span><span class="sxs-lookup"><span data-stu-id="d084b-112">_name_</span></span> <br/> |<span data-ttu-id="d084b-113">必須</span><span class="sxs-lookup"><span data-stu-id="d084b-113">Required</span></span>  <br/> |<span data-ttu-id="d084b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d084b-114">**String**</span></span> <br/> |<span data-ttu-id="d084b-115">有効なマスター シェイプの名前である、任意の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="d084b-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d084b-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="d084b-116">Return value</span></span>

<span data-ttu-id="d084b-117">番号</span><span class="sxs-lookup"><span data-stu-id="d084b-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d084b-118">解説</span><span class="sxs-lookup"><span data-stu-id="d084b-118">Remarks</span></span>

<span data-ttu-id="d084b-119">_名前_が付けられたマスターシェイプが文書のステンシルにある場合、パターンは、線のパターン、塗りつぶしのパターン、矢印の始点、または終点の矢印として適用されます。</span><span class="sxs-lookup"><span data-stu-id="d084b-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="d084b-120">この関数は常に 254 を返します。</span><span class="sxs-lookup"><span data-stu-id="d084b-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="d084b-121">例</span><span class="sxs-lookup"><span data-stu-id="d084b-121">Example</span></span>

<span data-ttu-id="d084b-122">USE("線路")</span><span class="sxs-lookup"><span data-stu-id="d084b-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="d084b-123">"線路" という名のマスター シェイプのパターンを、数式が含まれる図形に適用することにより、図形を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="d084b-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

