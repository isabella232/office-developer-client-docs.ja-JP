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
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349323"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="eb98a-103">[SubAddress] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="eb98a-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="eb98a-104">リンク先のターゲット図面内での位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb98a-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb98a-105">注釈</span><span class="sxs-lookup"><span data-stu-id="eb98a-105">Remarks</span></span>

<span data-ttu-id="eb98a-106">たとえば、[アドレス] セルが "Drawing1.vsdx" の場合、[SubAddress] セルは"Page-3" などのページ名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="eb98a-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="eb98a-107">[アドレス] セルが Microsoft Excel ファイル "Samples.xlsx" の場合、このセルの値は、ワークシート内のワークシートまたは範囲 ("Worksheet Functions" や "Sheet1!A1:D10".</span><span class="sxs-lookup"><span data-stu-id="eb98a-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="eb98a-108">[アドレス] セルが ""の場合、このセルの値は、"ソリューション" など、ドキュメント内の名前付きアンカー https://www.microsoft.com/office/ になります。</span><span class="sxs-lookup"><span data-stu-id="eb98a-108">If the Address cell is "https://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="eb98a-109">このセルの値は、[**ハイパーリンク**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**リンク**] グループで、[**ハイパーリンク**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="eb98a-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="eb98a-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SubAddress] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb98a-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb98a-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="eb98a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="eb98a-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="eb98a-112">Hyperlink.</span></span>  <span data-ttu-id="eb98a-113">*name*  .SubAddress where Hyperlink  *.name is the row*  name</span><span class="sxs-lookup"><span data-stu-id="eb98a-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="eb98a-114">プログラムからインデックスによって **[SubAddress]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb98a-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb98a-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb98a-115">Section index:</span></span>  <br/> |<span data-ttu-id="eb98a-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="eb98a-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="eb98a-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb98a-117">Row index:</span></span>  <br/> |<span data-ttu-id="eb98a-118">**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="eb98a-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="eb98a-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb98a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="eb98a-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="eb98a-120">**visHLinkSubAddress**</span></span> <br/> |
   

