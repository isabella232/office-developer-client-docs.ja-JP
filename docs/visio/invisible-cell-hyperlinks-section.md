---
title: '[Invisible] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: 図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805602"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="c8e07-103">[Invisible] セル ([ハイパーリンク] セクション)</span><span class="sxs-lookup"><span data-stu-id="c8e07-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="c8e07-104">図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c8e07-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="c8e07-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c8e07-105">**Value**</span></span>|<span data-ttu-id="c8e07-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c8e07-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8e07-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c8e07-107">TRUE</span></span>  <br/> |<span data-ttu-id="c8e07-108">ハイパーリンクは、ショートカット メニューのメニュー項目として表示されません。</span><span class="sxs-lookup"><span data-stu-id="c8e07-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="c8e07-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c8e07-109">FALSE</span></span>  <br/> |<span data-ttu-id="c8e07-110">ハイパーリンクは、ショートカット メニューのメニュー項目として表示されます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="c8e07-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8e07-111">注釈</span><span class="sxs-lookup"><span data-stu-id="c8e07-111">Remarks</span></span>

<span data-ttu-id="c8e07-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c8e07-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8e07-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="c8e07-113">Cell name:</span></span>  <br/> |<span data-ttu-id="c8e07-114">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="c8e07-114">Hyperlink.</span></span> <span data-ttu-id="c8e07-115">*名*です。ハイパーリンク *.name*は、行の名前が表示されません。</span><span class="sxs-lookup"><span data-stu-id="c8e07-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="c8e07-116">プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8e07-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8e07-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8e07-117">Section index:</span></span>  <br/> |<span data-ttu-id="c8e07-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="c8e07-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="c8e07-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8e07-119">Row index:</span></span>  <br/> |<span data-ttu-id="c8e07-120">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="c8e07-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c8e07-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8e07-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c8e07-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="c8e07-122">**visHLinkInvisible**</span></span> <br/> |
   

