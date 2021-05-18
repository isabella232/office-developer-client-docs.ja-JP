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
# <a name="textwidth-function"></a><span data-ttu-id="40bc3-103">TEXTWIDTH 関数</span><span class="sxs-lookup"><span data-stu-id="40bc3-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="40bc3-104">図形内の構成されたテキストの幅を返します。</span><span class="sxs-lookup"><span data-stu-id="40bc3-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="40bc3-105">構文</span><span class="sxs-lookup"><span data-stu-id="40bc3-105">Syntax</span></span>

<span data-ttu-id="40bc3-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\*\* [,maximumwidth]\* \*\* )</span><span class="sxs-lookup"><span data-stu-id="40bc3-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="40bc3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="40bc3-107">Parameters</span></span>

|<span data-ttu-id="40bc3-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="40bc3-108">**Name**</span></span>|<span data-ttu-id="40bc3-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="40bc3-109">**Required/Optional**</span></span>|<span data-ttu-id="40bc3-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="40bc3-110">**Data Type**</span></span>|<span data-ttu-id="40bc3-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="40bc3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="40bc3-112">_shapename!theText_</span><span class="sxs-lookup"><span data-stu-id="40bc3-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="40bc3-113">必須</span><span class="sxs-lookup"><span data-stu-id="40bc3-113">Required</span></span>  <br/> |<span data-ttu-id="40bc3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="40bc3-114">**String**</span></span> <br/> |<span data-ttu-id="40bc3-115">ターゲットとなる図形の [TheText] セルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="40bc3-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="40bc3-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="40bc3-116">_shapename!_</span></span> <span data-ttu-id="40bc3-117">は、テキストを取得する図形の名前です。</span><span class="sxs-lookup"><span data-stu-id="40bc3-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="40bc3-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="40bc3-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="40bc3-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="40bc3-119">Optional</span></span>  <br/> |<span data-ttu-id="40bc3-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="40bc3-120">**Numeric**</span></span> <br/> |<span data-ttu-id="40bc3-121">テキスト ブロックの最大幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="40bc3-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="40bc3-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="40bc3-122">Return value</span></span>

<span data-ttu-id="40bc3-123">文字列</span><span class="sxs-lookup"><span data-stu-id="40bc3-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40bc3-124">注釈</span><span class="sxs-lookup"><span data-stu-id="40bc3-124">Remarks</span></span>

<span data-ttu-id="40bc3-125">TEXTWIDTH 関数は、通常、格納するテキストのサイズに合わせて図形の幅を調整する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="40bc3-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="40bc3-126">_sheetN!_</span><span class="sxs-lookup"><span data-stu-id="40bc3-126">If  _sheetN!_</span></span> <span data-ttu-id="40bc3-127">を省略すると、既定の図形は現在の図形になります。</span><span class="sxs-lookup"><span data-stu-id="40bc3-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="40bc3-128">_maximumwidth を指定_ すると、結果は最大の範囲に収まるテキストの最長行 _になります_。</span><span class="sxs-lookup"><span data-stu-id="40bc3-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="40bc3-129">_maximumwidth を_ 省略すると、テキストの合計幅が返されます。</span><span class="sxs-lookup"><span data-stu-id="40bc3-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="40bc3-130">例</span><span class="sxs-lookup"><span data-stu-id="40bc3-130">Example</span></span>

<span data-ttu-id="40bc3-131">TEXTWIDTH(TheText)</span><span class="sxs-lookup"><span data-stu-id="40bc3-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="40bc3-132">現在の図形内にあるテキストの長さの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="40bc3-132">Returns the total length of the text in the current shape.</span></span> 
  

