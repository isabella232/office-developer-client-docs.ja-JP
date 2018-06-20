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
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805236"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="ae873-103">[Description] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="ae873-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="ae873-104">ハイパーリンクの説明文を表示します。</span><span class="sxs-lookup"><span data-stu-id="ae873-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ae873-105">注釈</span><span class="sxs-lookup"><span data-stu-id="ae873-105">Remarks</span></span>

<span data-ttu-id="ae873-106">ハイパーリンクに関するコメント (たとえば  "Link to our pricing Web site." など) は、このセルに格納します。</span><span class="sxs-lookup"><span data-stu-id="ae873-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing Web site."</span></span>
  
<span data-ttu-id="ae873-107">**[ハイパーリンク**] ダイアログ ボックスで、このセルの値を設定することもできます ([**挿入**] タブで**ハイパーリンク**をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="ae873-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="ae873-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[説明] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ae873-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae873-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="ae873-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ae873-110">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="ae873-110">Hyperlink.</span></span>  <span data-ttu-id="ae873-111">*名*です。説明するハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="ae873-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="ae873-112">*ハイパーリンク行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="ae873-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="ae873-113">プログラムから、インデックスによって [説明] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae873-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae873-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae873-114">Section index:</span></span>  <br/> |<span data-ttu-id="ae873-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="ae873-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="ae873-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae873-116">Row index:</span></span>  <br/> |<span data-ttu-id="ae873-117">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="ae873-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ae873-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae873-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ae873-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="ae873-119">**visHLinkDescription**</span></span> <br/> |
   

