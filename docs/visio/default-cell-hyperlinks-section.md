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
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805193"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="854c7-104">[Default] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="854c7-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="854c7-p102">図形またはページの既定のハイパーリンクを指定します。既定のハイパーリンクを設定するには、このセルの値を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="854c7-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="854c7-107">注釈</span><span class="sxs-lookup"><span data-stu-id="854c7-107">Remarks</span></span>

<span data-ttu-id="854c7-108">図形を選択すると、[**挿入**] タブで、**ハイパーリンク**をクリックすると、ハイパーリンクを選択すると、 **] をクリック**して既定のハイパーリンクを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="854c7-108">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**.</span></span> <span data-ttu-id="854c7-109">既定のハイパーリンクは太字で表示されます。</span><span class="sxs-lookup"><span data-stu-id="854c7-109">The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="854c7-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Default] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="854c7-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="854c7-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="854c7-111">Cell name:</span></span>  <br/> |<span data-ttu-id="854c7-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="854c7-112">Hyperlink.</span></span> <span data-ttu-id="854c7-113">*名*です。既定の場所のハイパーリンクです。</span><span class="sxs-lookup"><span data-stu-id="854c7-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="854c7-114">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="854c7-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="854c7-115">プログラムから、インデックスによって [Default] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="854c7-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="854c7-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="854c7-116">Section index:</span></span>  <br/> |<span data-ttu-id="854c7-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="854c7-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="854c7-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="854c7-118">Row index:</span></span>  <br/> |<span data-ttu-id="854c7-119">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="854c7-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="854c7-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="854c7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="854c7-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="854c7-121">**visHLinkDefault**</span></span> <br/> |
   

