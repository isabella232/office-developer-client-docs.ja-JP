---
title: '[Description] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: ハイパーリンクの説明文を表示します。
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360243"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="2ec28-103">[Description] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="2ec28-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="2ec28-104">ハイパーリンクの説明文を表示します。</span><span class="sxs-lookup"><span data-stu-id="2ec28-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2ec28-105">注釈</span><span class="sxs-lookup"><span data-stu-id="2ec28-105">Remarks</span></span>

<span data-ttu-id="2ec28-106">ハイパーリンクに関するコメントを格納するには、このセルを使用します。たとえば、「価格設定 Web サイトへのリンク」などです。</span><span class="sxs-lookup"><span data-stu-id="2ec28-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="2ec28-107">このセルの値は、[**ハイパーリンク**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**ハイパーリンク**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="2ec28-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="2ec28-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2ec28-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ec28-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="2ec28-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2ec28-110">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="2ec28-110">Hyperlink.</span></span>  <span data-ttu-id="2ec28-111">*Name*  .[ハイパーリンク] の説明。</span><span class="sxs-lookup"><span data-stu-id="2ec28-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="2ec28-112">*名前*  はハイパーリンク行の名前です。</span><span class="sxs-lookup"><span data-stu-id="2ec28-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="2ec28-113">プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ec28-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ec28-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ec28-114">Section index:</span></span>  <br/> |<span data-ttu-id="2ec28-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="2ec28-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="2ec28-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ec28-116">Row index:</span></span>  <br/> |<span data-ttu-id="2ec28-117">**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2ec28-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2ec28-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ec28-118">Cell index:</span></span>  <br/> |<span data-ttu-id="2ec28-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="2ec28-119">**visHLinkDescription**</span></span> <br/> |
   

