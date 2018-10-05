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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396625"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="c68d5-103">[Description] セル ([ハイパーリンク] セクション)</span><span class="sxs-lookup"><span data-stu-id="c68d5-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="c68d5-104">ハイパーリンクの説明文を表示します。</span><span class="sxs-lookup"><span data-stu-id="c68d5-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c68d5-105">注釈</span><span class="sxs-lookup"><span data-stu-id="c68d5-105">Remarks</span></span>

<span data-ttu-id="c68d5-106">このセルを使用して、ハイパーリンクに関するコメントを保存するにはたとえば、「へのリンク、価格設定の web サイト。」</span><span class="sxs-lookup"><span data-stu-id="c68d5-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="c68d5-107">このセルの値は、[**ハイパーリンク**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**ハイパーリンク**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="c68d5-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="c68d5-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c68d5-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c68d5-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="c68d5-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c68d5-110">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="c68d5-110">Hyperlink.</span></span>  <span data-ttu-id="c68d5-111">*名*です。説明するハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="c68d5-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="c68d5-112">*ハイパーリンク行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="c68d5-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="c68d5-113">プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c68d5-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c68d5-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c68d5-114">Section index:</span></span>  <br/> |<span data-ttu-id="c68d5-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="c68d5-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="c68d5-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c68d5-116">Row index:</span></span>  <br/> |<span data-ttu-id="c68d5-117">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="c68d5-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c68d5-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c68d5-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c68d5-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="c68d5-119">**visHLinkDescription**</span></span> <br/> |
   

