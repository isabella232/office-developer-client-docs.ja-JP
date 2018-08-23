---
title: '[SubAddress] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: リンク先のターゲット図面内での位置を指定します。
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806595"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="be2b5-103">[SubAddress] セル ([ハイパーリンク] セクション)</span><span class="sxs-lookup"><span data-stu-id="be2b5-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="be2b5-104">リンク先のターゲット図面内での位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="be2b5-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be2b5-105">注釈</span><span class="sxs-lookup"><span data-stu-id="be2b5-105">Remarks</span></span>

<span data-ttu-id="be2b5-106">たとえば、アドレスのセルが"Drawing1.vsdx"の場合は、サブアドレスのセルは「ページ 3」などのページ名を指定できます。 します</span><span class="sxs-lookup"><span data-stu-id="be2b5-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="be2b5-107">ワークシートまたは範囲を「ワークシート関数」や「Sheet1 など、ワークシート内セルの値は、アドレスのセルが Excel のファイル"Samples.xlsx"の場合は、!範囲 A1: D10"です。</span><span class="sxs-lookup"><span data-stu-id="be2b5-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="be2b5-108">場合は、[Address] セルは、"http://www.microsoft.com/office/"、このセルの値は「ソリューション」など、ドキュメント内で名前付きアンカーをすることができます。</span><span class="sxs-lookup"><span data-stu-id="be2b5-108">If the Address cell is "http://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="be2b5-109">このセルの値は、[**ハイパーリンク**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**リンク**] グループで、[**ハイパーリンク**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="be2b5-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="be2b5-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SubAddress] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="be2b5-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be2b5-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="be2b5-111">Cell name:</span></span>  <br/> | <span data-ttu-id="be2b5-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="be2b5-112">Hyperlink.</span></span>  <span data-ttu-id="be2b5-113">*名*です。サブアドレスのハイパーリンクの *.name*と行の名前があります。</span><span class="sxs-lookup"><span data-stu-id="be2b5-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="be2b5-114">プログラムから、インデックスによって [ **SubAddress** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="be2b5-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be2b5-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="be2b5-115">Section index:</span></span>  <br/> |<span data-ttu-id="be2b5-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="be2b5-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="be2b5-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="be2b5-117">Row index:</span></span>  <br/> |<span data-ttu-id="be2b5-118">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="be2b5-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="be2b5-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="be2b5-119">Cell index:</span></span>  <br/> |<span data-ttu-id="be2b5-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="be2b5-120">**visHLinkSubAddress**</span></span> <br/> |
   

