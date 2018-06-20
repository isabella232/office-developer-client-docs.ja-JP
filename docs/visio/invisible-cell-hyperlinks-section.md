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
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="66e7c-103">[Invisible] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="66e7c-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="66e7c-104">図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="66e7c-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="66e7c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="66e7c-105">**Value**</span></span>|<span data-ttu-id="66e7c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="66e7c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66e7c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="66e7c-107">TRUE</span></span>  <br/> |<span data-ttu-id="66e7c-108">ハイパーリンクは、ショートカット メニューのメニュー項目として表示されません。</span><span class="sxs-lookup"><span data-stu-id="66e7c-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="66e7c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="66e7c-109">FALSE</span></span>  <br/> |<span data-ttu-id="66e7c-110">ハイパーリンクは、ショートカット メニューのメニュー項目として表示されます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="66e7c-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66e7c-111">注釈</span><span class="sxs-lookup"><span data-stu-id="66e7c-111">Remarks</span></span>

<span data-ttu-id="66e7c-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって非表示のセルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="66e7c-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66e7c-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="66e7c-113">Cell name:</span></span>  <br/> |<span data-ttu-id="66e7c-114">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="66e7c-114">Hyperlink.</span></span> <span data-ttu-id="66e7c-115">*名*です。ハイパーリンク *.name*は、行の名前が表示されません。</span><span class="sxs-lookup"><span data-stu-id="66e7c-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="66e7c-116">プログラムから、インデックスによって [Invisible] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="66e7c-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66e7c-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="66e7c-117">Section index:</span></span>  <br/> |<span data-ttu-id="66e7c-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="66e7c-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="66e7c-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="66e7c-119">Row index:</span></span>  <br/> |<span data-ttu-id="66e7c-120">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="66e7c-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="66e7c-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="66e7c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="66e7c-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="66e7c-122">**visHLinkInvisible**</span></span> <br/> |
   

