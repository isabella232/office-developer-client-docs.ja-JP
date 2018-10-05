---
title: '[NewWindow] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: ハイパーリンクを新しいウィンドウで開くかどうかを指定します。
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396338"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="95fc6-103">[NewWindow] セル ([ハイパーリンク] セクション)</span><span class="sxs-lookup"><span data-stu-id="95fc6-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="95fc6-104">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="95fc6-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="95fc6-105">**値**</span><span class="sxs-lookup"><span data-stu-id="95fc6-105">**Value**</span></span>|<span data-ttu-id="95fc6-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="95fc6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="95fc6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="95fc6-107">TRUE</span></span>  <br/> | <span data-ttu-id="95fc6-108">新しいウィンドウでリンク先のページ、ドキュメント、または web サイトを開きます。</span><span class="sxs-lookup"><span data-stu-id="95fc6-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="95fc6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="95fc6-109">FALSE</span></span>  <br/> | <span data-ttu-id="95fc6-p101">既定値です。ハイパーリンク用に新しいウィンドウを開きません。</span><span class="sxs-lookup"><span data-stu-id="95fc6-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95fc6-112">備考</span><span class="sxs-lookup"><span data-stu-id="95fc6-112">Remarks</span></span>

<span data-ttu-id="95fc6-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NewWindow] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95fc6-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95fc6-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="95fc6-114">Cell name:</span></span>  <br/> | <span data-ttu-id="95fc6-115">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="95fc6-115">Hyperlink.</span></span>  <span data-ttu-id="95fc6-116">*名*です。NewWindow いるハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="95fc6-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="95fc6-117">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="95fc6-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="95fc6-118">プログラムから、インデックスによって [NewWindow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="95fc6-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95fc6-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="95fc6-119">Section index:</span></span>  <br/> |<span data-ttu-id="95fc6-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="95fc6-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="95fc6-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="95fc6-121">Row index:</span></span>  <br/> |<span data-ttu-id="95fc6-122">**visRow1stHyperlink** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="95fc6-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="95fc6-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="95fc6-123">Cell index:</span></span>  <br/> |<span data-ttu-id="95fc6-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="95fc6-124">**visHLinkNewWin**</span></span> <br/> |
   

