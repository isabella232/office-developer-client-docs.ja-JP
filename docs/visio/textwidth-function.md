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
description: 図形で構成されたテキストの幅を返します。
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806627"
---
# <a name="textwidth-function"></a><span data-ttu-id="3ee24-103">TEXTWIDTH 関数</span><span class="sxs-lookup"><span data-stu-id="3ee24-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="3ee24-104">図形で構成されたテキストの幅を返します。</span><span class="sxs-lookup"><span data-stu-id="3ee24-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3ee24-105">構文</span><span class="sxs-lookup"><span data-stu-id="3ee24-105">Syntax</span></span>

<span data-ttu-id="3ee24-106">TEXTWIDTH (* **なります。[Thetext]* * * * * *[] maximumwidth* * *)</span><span class="sxs-lookup"><span data-stu-id="3ee24-106">TEXTWIDTH(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3ee24-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3ee24-107">Parameters</span></span>

|<span data-ttu-id="3ee24-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="3ee24-108">**Name**</span></span>|<span data-ttu-id="3ee24-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3ee24-109">**Required/Optional**</span></span>|<span data-ttu-id="3ee24-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3ee24-110">**Data Type**</span></span>|<span data-ttu-id="3ee24-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3ee24-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3ee24-112">_なります! テキスト_</span><span class="sxs-lookup"><span data-stu-id="3ee24-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="3ee24-113">必須</span><span class="sxs-lookup"><span data-stu-id="3ee24-113">Required</span></span>  <br/> |<span data-ttu-id="3ee24-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="3ee24-114">**String**</span></span> <br/> |<span data-ttu-id="3ee24-115">セルへの参照では、接続先の図形の [thetext] という名前です。</span><span class="sxs-lookup"><span data-stu-id="3ee24-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="3ee24-116">_なります!_</span><span class="sxs-lookup"><span data-stu-id="3ee24-116">_shapename!_</span></span> <span data-ttu-id="3ee24-117">テキストを取得する図形の名前です。</span><span class="sxs-lookup"><span data-stu-id="3ee24-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="3ee24-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="3ee24-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="3ee24-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="3ee24-119">Optional</span></span>  <br/> |<span data-ttu-id="3ee24-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="3ee24-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3ee24-121">テキスト ブロックの最大幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="3ee24-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3ee24-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="3ee24-122">Return value</span></span>

<span data-ttu-id="3ee24-123">String</span><span class="sxs-lookup"><span data-stu-id="3ee24-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ee24-124">注釈</span><span class="sxs-lookup"><span data-stu-id="3ee24-124">Remarks</span></span>

<span data-ttu-id="3ee24-125">TEXTWIDTH 関数は、通常、格納するテキストのサイズに合わせて図形の幅を調整する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="3ee24-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="3ee24-126">場合_sheetN!_</span><span class="sxs-lookup"><span data-stu-id="3ee24-126">If  _sheetN!_</span></span> <span data-ttu-id="3ee24-127">省略すると、現在の図形は、オートシェイプの既定値です。</span><span class="sxs-lookup"><span data-stu-id="3ee24-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="3ee24-128">_Maximumwidth_が指定されている場合は_maximumwidth_内に収まっているテキストの最長の行になります。</span><span class="sxs-lookup"><span data-stu-id="3ee24-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="3ee24-129">_Maximumwidth_を省略すると、テキストの幅の合計になります。</span><span class="sxs-lookup"><span data-stu-id="3ee24-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3ee24-130">例</span><span class="sxs-lookup"><span data-stu-id="3ee24-130">Example</span></span>

<span data-ttu-id="3ee24-131">TEXTWIDTH(TheText)</span><span class="sxs-lookup"><span data-stu-id="3ee24-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="3ee24-132">現在の図形内にあるテキストの長さの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="3ee24-132">Returns the total length of the text in the current shape.</span></span> 
  

