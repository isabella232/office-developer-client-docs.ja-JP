---
title: '[Default] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: 図形またはページの既定のハイパーリンクを指定します。既定のハイパーリンクを設定するには、このセルの値を TRUE に設定します。
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434355"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="29453-104">[Default] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="29453-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="29453-p102">図形またはページの既定のハイパーリンクを指定します。既定のハイパーリンクを設定するには、このセルの値を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="29453-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29453-107">注釈</span><span class="sxs-lookup"><span data-stu-id="29453-107">Remarks</span></span>

<span data-ttu-id="29453-p103">既定のハイパーリンクは、図形をクリックして [**挿入**] タブの [**ハイパーリンク**] をクリックし、[**既定値**] をクリックすることで設定することもできます。既定のハイパーリンクは太字で表示されます。</span><span class="sxs-lookup"><span data-stu-id="29453-p103">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**. The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="29453-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Default] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="29453-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29453-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="29453-111">Cell name:</span></span>  <br/> |<span data-ttu-id="29453-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="29453-112">Hyperlink.</span></span> <span data-ttu-id="29453-113">*名前*です。既定のハイパーリンク先。</span><span class="sxs-lookup"><span data-stu-id="29453-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="29453-114">*name*には、行の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="29453-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="29453-115">プログラムから、インデックスによって [Default] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="29453-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29453-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="29453-116">Section index:</span></span>  <br/> |<span data-ttu-id="29453-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="29453-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="29453-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="29453-118">Row index:</span></span>  <br/> |<span data-ttu-id="29453-119">**visRow1stHyperlink** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="29453-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="29453-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="29453-120">Cell index:</span></span>  <br/> |<span data-ttu-id="29453-121">**vishlinkdefault**</span><span class="sxs-lookup"><span data-stu-id="29453-121">**visHLinkDefault**</span></span> <br/> |
   

