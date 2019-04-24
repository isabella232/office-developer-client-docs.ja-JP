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
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="62034-103">[SubAddress] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="62034-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="62034-104">リンク先のターゲット図面内での位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="62034-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62034-105">解説</span><span class="sxs-lookup"><span data-stu-id="62034-105">Remarks</span></span>

<span data-ttu-id="62034-106">たとえば、アドレスセルが "Drawing1" の場合、サブアドレスセルは "ページ-3" などのページ名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="62034-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="62034-107">[Address] セルが Microsoft Excel ファイル "Samples" の場合、このセルの値は、ワークシート内のワークシートまたはセル範囲 ("worksheet 関数"、"Sheet1!" など) にすることができます。A1: D10</span><span class="sxs-lookup"><span data-stu-id="62034-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="62034-108">[Address] セルが "https://www.microsoft.com/office/" の場合、このセルの値は、"solutions" など、ドキュメント内の名前付きアンカーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="62034-108">If the Address cell is "https://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="62034-109">このセルの値は、[**ハイパーリンク**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**リンク**] グループで、[**ハイパーリンク**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="62034-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="62034-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SubAddress] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="62034-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62034-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="62034-111">Cell name:</span></span>  <br/> | <span data-ttu-id="62034-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="62034-112">Hyperlink.</span></span>  <span data-ttu-id="62034-113">*名前*です。サブアドレスハイパーリンクの名前は、行名です *。*</span><span class="sxs-lookup"><span data-stu-id="62034-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="62034-114">プログラムから、インデックスによって [サブ**アドレス**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62034-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62034-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="62034-115">Section index:</span></span>  <br/> |<span data-ttu-id="62034-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="62034-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="62034-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="62034-117">Row index:</span></span>  <br/> |<span data-ttu-id="62034-118">**visRow1stHyperlink** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="62034-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="62034-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="62034-119">Cell index:</span></span>  <br/> |<span data-ttu-id="62034-120">**vishlinksubaddress アドレス**</span><span class="sxs-lookup"><span data-stu-id="62034-120">**visHLinkSubAddress**</span></span> <br/> |
   

