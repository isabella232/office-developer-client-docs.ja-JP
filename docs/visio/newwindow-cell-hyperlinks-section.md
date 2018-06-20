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
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="8ad89-103">[NewWindow] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="8ad89-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="8ad89-104">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8ad89-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="8ad89-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8ad89-105">**Value**</span></span>|<span data-ttu-id="8ad89-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8ad89-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8ad89-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8ad89-107">TRUE</span></span>  <br/> | <span data-ttu-id="8ad89-108">リンクされたページ、図面、または Web サイトを新しいウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="8ad89-108">Open the linked page, document, or Web site in a new window.</span></span>  <br/> |
| <span data-ttu-id="8ad89-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8ad89-109">FALSE</span></span>  <br/> | <span data-ttu-id="8ad89-p101">既定値です。ハイパーリンク用に新しいウィンドウを開きません。</span><span class="sxs-lookup"><span data-stu-id="8ad89-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ad89-112">備考</span><span class="sxs-lookup"><span data-stu-id="8ad89-112">Remarks</span></span>

<span data-ttu-id="8ad89-113">別の数式または**CellsU**プロパティを使用したプログラムからは、名前によって、[NewWindow] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8ad89-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ad89-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="8ad89-114">Cell name:</span></span>  <br/> | <span data-ttu-id="8ad89-115">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="8ad89-115">Hyperlink.</span></span>  <span data-ttu-id="8ad89-116">*名*です。NewWindow いるハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="8ad89-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="8ad89-117">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="8ad89-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="8ad89-118">プログラムから、インデックスによって [NewWindow] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8ad89-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ad89-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ad89-119">Section index:</span></span>  <br/> |<span data-ttu-id="8ad89-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="8ad89-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="8ad89-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ad89-121">Row index:</span></span>  <br/> |<span data-ttu-id="8ad89-122">**visRow1stHyperlink** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="8ad89-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="8ad89-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ad89-123">Cell index:</span></span>  <br/> |<span data-ttu-id="8ad89-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="8ad89-124">**visHLinkNewWin**</span></span> <br/> |
   

