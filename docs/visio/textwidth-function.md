---
title: TEXTWIDTH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: 図形内の構成されたテキストの幅を返します。
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422034"
---
# <a name="textwidth-function"></a><span data-ttu-id="79727-103">TEXTWIDTH 関数</span><span class="sxs-lookup"><span data-stu-id="79727-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="79727-104">図形内の構成されたテキストの幅を返します。</span><span class="sxs-lookup"><span data-stu-id="79727-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="79727-105">構文</span><span class="sxs-lookup"><span data-stu-id="79727-105">Syntax</span></span>

<span data-ttu-id="79727-106">TEXTWIDTH (\* \* 図形の場合) \*\* テキスト \* \* \* \* *[, maximumwidth]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="79727-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="79727-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="79727-107">Parameters</span></span>

|<span data-ttu-id="79727-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="79727-108">**Name**</span></span>|<span data-ttu-id="79727-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="79727-109">**Required/Optional**</span></span>|<span data-ttu-id="79727-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="79727-110">**Data Type**</span></span>|<span data-ttu-id="79727-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="79727-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="79727-112">_offename! テキスト_</span><span class="sxs-lookup"><span data-stu-id="79727-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="79727-113">必須</span><span class="sxs-lookup"><span data-stu-id="79727-113">Required</span></span>  <br/> |<span data-ttu-id="79727-114">**String**</span><span class="sxs-lookup"><span data-stu-id="79727-114">**String**</span></span> <br/> |<span data-ttu-id="79727-115">ターゲットとなる図形の [TheText] セルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="79727-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="79727-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="79727-116">_shapename!_</span></span> <span data-ttu-id="79727-117">は、テキストを取得する図形の名前です。</span><span class="sxs-lookup"><span data-stu-id="79727-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="79727-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="79727-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="79727-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="79727-119">Optional</span></span>  <br/> |<span data-ttu-id="79727-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="79727-120">**Numeric**</span></span> <br/> |<span data-ttu-id="79727-121">テキスト ブロックの最大幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="79727-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="79727-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="79727-122">Return value</span></span>

<span data-ttu-id="79727-123">文字列</span><span class="sxs-lookup"><span data-stu-id="79727-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="79727-124">注釈</span><span class="sxs-lookup"><span data-stu-id="79727-124">Remarks</span></span>

<span data-ttu-id="79727-125">TEXTWIDTH 関数は、通常、格納するテキストのサイズに合わせて図形の幅を調整する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="79727-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="79727-126">_\n_</span><span class="sxs-lookup"><span data-stu-id="79727-126">If  _sheetN!_</span></span> <span data-ttu-id="79727-127">を省略すると、既定の図形は現在の図形になります。</span><span class="sxs-lookup"><span data-stu-id="79727-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="79727-128">_maximumwidth_が指定されている場合、結果は、 _maximumwidth_に収まる最大のテキスト行になります。</span><span class="sxs-lookup"><span data-stu-id="79727-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="79727-129">_maximumwidth_を省略すると、結果はテキストの幅の合計になります。</span><span class="sxs-lookup"><span data-stu-id="79727-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="79727-130">例</span><span class="sxs-lookup"><span data-stu-id="79727-130">Example</span></span>

<span data-ttu-id="79727-131">TEXTWIDTH (テキスト)</span><span class="sxs-lookup"><span data-stu-id="79727-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="79727-132">現在の図形内にあるテキストの長さの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="79727-132">Returns the total length of the text in the current shape.</span></span> 
  

