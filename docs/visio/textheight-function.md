---
title: TEXTHEIGHT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: テキスト行を超えている maximumwidth 図形で構成されたテキストの高さを返しません。
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806629"
---
# <a name="textheight-function"></a><span data-ttu-id="56bdf-103">TEXTHEIGHT 関数</span><span class="sxs-lookup"><span data-stu-id="56bdf-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="56bdf-104">テキスト行を超えている_maximumwidth_図形で構成されたテキストの高さを返しません。</span><span class="sxs-lookup"><span data-stu-id="56bdf-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="56bdf-105">構文</span><span class="sxs-lookup"><span data-stu-id="56bdf-105">Syntax</span></span>

<span data-ttu-id="56bdf-106">TEXTHEIGHT (* **なります。[Thetext]* * * * * *[] maximumwidth* * *)</span><span class="sxs-lookup"><span data-stu-id="56bdf-106">TEXTHEIGHT(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="56bdf-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="56bdf-107">Parameters</span></span>

|<span data-ttu-id="56bdf-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="56bdf-108">**Name**</span></span>|<span data-ttu-id="56bdf-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="56bdf-109">**Required/Optional**</span></span>|<span data-ttu-id="56bdf-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="56bdf-110">**Data Type**</span></span>|<span data-ttu-id="56bdf-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="56bdf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="56bdf-112">_なります! テキスト_</span><span class="sxs-lookup"><span data-stu-id="56bdf-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="56bdf-113">必須</span><span class="sxs-lookup"><span data-stu-id="56bdf-113">Required</span></span>  <br/> |<span data-ttu-id="56bdf-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="56bdf-114">**String**</span></span> <br/> |<span data-ttu-id="56bdf-115">セルへの参照では、接続先の図形の [thetext] という名前です。</span><span class="sxs-lookup"><span data-stu-id="56bdf-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="56bdf-116">_なります!_</span><span class="sxs-lookup"><span data-stu-id="56bdf-116">_shapename!_</span></span> <span data-ttu-id="56bdf-117">テキストを取得する図形の名前です。</span><span class="sxs-lookup"><span data-stu-id="56bdf-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="56bdf-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="56bdf-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="56bdf-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="56bdf-119">Optional</span></span>  <br/> |<span data-ttu-id="56bdf-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="56bdf-120">**Numeric**</span></span> <br/> |<span data-ttu-id="56bdf-121">テキスト ブロックの最大幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="56bdf-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="56bdf-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="56bdf-122">Return value</span></span>

<span data-ttu-id="56bdf-123">String</span><span class="sxs-lookup"><span data-stu-id="56bdf-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56bdf-124">注釈</span><span class="sxs-lookup"><span data-stu-id="56bdf-124">Remarks</span></span>

<span data-ttu-id="56bdf-p102">戻り値として、テキストの前後のスペースを含む高さ、行間隔、およびテキスト ブロックの上下の余白が返されます。この関数は、通常、格納するテキストのサイズに合わせて図形の高さを調整する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="56bdf-p102">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins. This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="56bdf-127">例</span><span class="sxs-lookup"><span data-stu-id="56bdf-127">Example</span></span>

<span data-ttu-id="56bdf-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span><span class="sxs-lookup"><span data-stu-id="56bdf-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="56bdf-129">図形の幅から 0.5 インチ差し引いた幅で折り返した場合の、テキストの高さを返します。</span><span class="sxs-lookup"><span data-stu-id="56bdf-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

