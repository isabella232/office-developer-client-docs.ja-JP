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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422825"
---
# <a name="use-function"></a><span data-ttu-id="a403c-103">USE 関数</span><span class="sxs-lookup"><span data-stu-id="a403c-103">USE Function</span></span>

<span data-ttu-id="a403c-104">[linepattern]、[fillpattern]、[beginarrow]、または [endarrow] セルに配置されたときに、name という_名前_の線パターン、塗りつぶしパターン、または線の端点を図形に適用します。</span><span class="sxs-lookup"><span data-stu-id="a403c-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a403c-105">構文</span><span class="sxs-lookup"><span data-stu-id="a403c-105">Syntax</span></span>

<span data-ttu-id="a403c-106">USE ("\* \* *name* \* \*")</span><span class="sxs-lookup"><span data-stu-id="a403c-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a403c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a403c-107">Parameters</span></span>

|<span data-ttu-id="a403c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a403c-108">**Name**</span></span>|<span data-ttu-id="a403c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a403c-109">**Required/Optional**</span></span>|<span data-ttu-id="a403c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a403c-110">**Data Type**</span></span>|<span data-ttu-id="a403c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a403c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a403c-112">_name_</span><span class="sxs-lookup"><span data-stu-id="a403c-112">_name_</span></span> <br/> |<span data-ttu-id="a403c-113">必須</span><span class="sxs-lookup"><span data-stu-id="a403c-113">Required</span></span>  <br/> |<span data-ttu-id="a403c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a403c-114">**String**</span></span> <br/> |<span data-ttu-id="a403c-115">有効なマスター シェイプの名前である、任意の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="a403c-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a403c-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="a403c-116">Return value</span></span>

<span data-ttu-id="a403c-117">数値</span><span class="sxs-lookup"><span data-stu-id="a403c-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a403c-118">注釈</span><span class="sxs-lookup"><span data-stu-id="a403c-118">Remarks</span></span>

<span data-ttu-id="a403c-119">_名前_が付けられたマスターシェイプが文書のステンシルにある場合、パターンは、線のパターン、塗りつぶしのパターン、矢印の始点、または終点の矢印として適用されます。</span><span class="sxs-lookup"><span data-stu-id="a403c-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="a403c-120">この関数は常に 254 を返します。</span><span class="sxs-lookup"><span data-stu-id="a403c-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="a403c-121">例</span><span class="sxs-lookup"><span data-stu-id="a403c-121">Example</span></span>

<span data-ttu-id="a403c-122">USE("線路")</span><span class="sxs-lookup"><span data-stu-id="a403c-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="a403c-123">"線路" という名のマスター シェイプのパターンを、数式が含まれる図形に適用することにより、図形を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="a403c-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

