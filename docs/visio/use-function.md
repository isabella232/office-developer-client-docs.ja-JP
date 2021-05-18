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
description: LinePattern、FillPattern、BeginArrow、または EndArrow セルに配置すると、名前と呼ばれる線のパターン、塗りつぶしパターン、または線の端を図形に適用します。
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422825"
---
# <a name="use-function"></a><span data-ttu-id="2211f-103">USE 関数</span><span class="sxs-lookup"><span data-stu-id="2211f-103">USE Function</span></span>

<span data-ttu-id="2211f-104">LinePattern、FillPattern、BeginArrow、または EndArrow セルに配置すると、名前と呼ばれる線のパターン、塗りつぶしパターン、または線の端を図形に適用します。 </span><span class="sxs-lookup"><span data-stu-id="2211f-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2211f-105">構文</span><span class="sxs-lookup"><span data-stu-id="2211f-105">Syntax</span></span>

<span data-ttu-id="2211f-106">USE(" \*\* *name* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="2211f-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2211f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2211f-107">Parameters</span></span>

|<span data-ttu-id="2211f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="2211f-108">**Name**</span></span>|<span data-ttu-id="2211f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="2211f-109">**Required/Optional**</span></span>|<span data-ttu-id="2211f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="2211f-110">**Data Type**</span></span>|<span data-ttu-id="2211f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2211f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2211f-112">_name_</span><span class="sxs-lookup"><span data-stu-id="2211f-112">_name_</span></span> <br/> |<span data-ttu-id="2211f-113">必須</span><span class="sxs-lookup"><span data-stu-id="2211f-113">Required</span></span>  <br/> |<span data-ttu-id="2211f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2211f-114">**String**</span></span> <br/> |<span data-ttu-id="2211f-115">有効なマスター シェイプの名前である、任意の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="2211f-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2211f-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="2211f-116">Return value</span></span>

<span data-ttu-id="2211f-117">番号</span><span class="sxs-lookup"><span data-stu-id="2211f-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2211f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="2211f-118">Remarks</span></span>

<span data-ttu-id="2211f-119">文書の文書ステンシルにマスター名が存在する場合、パターンは線のパターン、塗りつぶしパターン、開始矢印、または終了矢印として適用されます。</span><span class="sxs-lookup"><span data-stu-id="2211f-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="2211f-120">この関数は常に 254 を返します。</span><span class="sxs-lookup"><span data-stu-id="2211f-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="2211f-121">例</span><span class="sxs-lookup"><span data-stu-id="2211f-121">Example</span></span>

<span data-ttu-id="2211f-122">USE("線路")</span><span class="sxs-lookup"><span data-stu-id="2211f-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="2211f-123">"線路" という名のマスター シェイプのパターンを、数式が含まれる図形に適用することにより、図形を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="2211f-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

