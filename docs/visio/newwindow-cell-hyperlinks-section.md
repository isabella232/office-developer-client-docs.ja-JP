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
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805919"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="37d06-103">[NewWindow] セル ([ハイパーリンク] セクション)</span><span class="sxs-lookup"><span data-stu-id="37d06-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="37d06-104">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="37d06-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="37d06-105">**値**</span><span class="sxs-lookup"><span data-stu-id="37d06-105">**Value**</span></span>|<span data-ttu-id="37d06-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="37d06-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="37d06-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="37d06-107">TRUE</span></span>  <br/> | <span data-ttu-id="37d06-108">リンクされたページ、図面、または Web サイトを新しいウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="37d06-108">Open the linked page, document, or Web site in a new window.</span></span>  <br/> |
| <span data-ttu-id="37d06-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="37d06-109">FALSE</span></span>  <br/> | <span data-ttu-id="37d06-p101">既定値です。ハイパーリンク用に新しいウィンドウを開きません。</span><span class="sxs-lookup"><span data-stu-id="37d06-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37d06-112">備考</span><span class="sxs-lookup"><span data-stu-id="37d06-112">Remarks</span></span>

<span data-ttu-id="37d06-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NewWindow] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="37d06-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37d06-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="37d06-114">Cell name:</span></span>  <br/> | <span data-ttu-id="37d06-115">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="37d06-115">Hyperlink.</span></span>  <span data-ttu-id="37d06-116">*名*です。NewWindow いるハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="37d06-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="37d06-117">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="37d06-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="37d06-118">プログラムから、インデックスによって [NewWindow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="37d06-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37d06-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="37d06-119">Section index:</span></span>  <br/> |<span data-ttu-id="37d06-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="37d06-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="37d06-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="37d06-121">Row index:</span></span>  <br/> |<span data-ttu-id="37d06-122">**visRow1stHyperlink** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="37d06-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="37d06-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="37d06-123">Cell index:</span></span>  <br/> |<span data-ttu-id="37d06-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="37d06-124">**visHLinkNewWin**</span></span> <br/> |
   

