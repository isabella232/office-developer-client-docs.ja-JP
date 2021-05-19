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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342232"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="ec806-103">[NewWindow] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="ec806-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="ec806-104">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec806-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="ec806-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ec806-105">**Value**</span></span>|<span data-ttu-id="ec806-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ec806-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ec806-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ec806-107">TRUE</span></span>  <br/> | <span data-ttu-id="ec806-108">リンクされたページ、ドキュメント、または Web サイトを新しいウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="ec806-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="ec806-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ec806-109">FALSE</span></span>  <br/> | <span data-ttu-id="ec806-p101">既定値です。ハイパーリンク用に新しいウィンドウを開きません。</span><span class="sxs-lookup"><span data-stu-id="ec806-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec806-112">注釈</span><span class="sxs-lookup"><span data-stu-id="ec806-112">Remarks</span></span>

<span data-ttu-id="ec806-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NewWindow] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec806-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec806-114">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ec806-114">Cell name:</span></span>  <br/> | <span data-ttu-id="ec806-115">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="ec806-115">Hyperlink.</span></span>  <span data-ttu-id="ec806-116">*Name*  .NewWindow where Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="ec806-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="ec806-117">*名前*  は行名です</span><span class="sxs-lookup"><span data-stu-id="ec806-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="ec806-118">プログラムから、インデックスによって [NewWindow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec806-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec806-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ec806-119">Section index:</span></span>  <br/> |<span data-ttu-id="ec806-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="ec806-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="ec806-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ec806-121">Row index:</span></span>  <br/> |<span data-ttu-id="ec806-122">**visRow1stHyperlink**  +  *i* *=* 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="ec806-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="ec806-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ec806-123">Cell index:</span></span>  <br/> |<span data-ttu-id="ec806-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="ec806-124">**visHLinkNewWin**</span></span> <br/> |
   

