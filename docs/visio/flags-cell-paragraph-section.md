---
title: '[Flags] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: テキストの方向が左から右か、右から左かを示します。
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805387"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="73b0b-103">[Flags] セル ([段落] セクション)</span><span class="sxs-lookup"><span data-stu-id="73b0b-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="73b0b-104">テキストの方向が左から右か、右から左かを示します。</span><span class="sxs-lookup"><span data-stu-id="73b0b-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="73b0b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="73b0b-105">**Value**</span></span>|<span data-ttu-id="73b0b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="73b0b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73b0b-107">0</span><span class="sxs-lookup"><span data-stu-id="73b0b-107">0</span></span>  <br/> |<span data-ttu-id="73b0b-108">テキストの方向は、左から右です (既定値)。</span><span class="sxs-lookup"><span data-stu-id="73b0b-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="73b0b-109">1</span><span class="sxs-lookup"><span data-stu-id="73b0b-109">1</span></span>  <br/> |<span data-ttu-id="73b0b-110">テキストの方向は、右から左です。</span><span class="sxs-lookup"><span data-stu-id="73b0b-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b0b-111">注釈</span><span class="sxs-lookup"><span data-stu-id="73b0b-111">Remarks</span></span>

<span data-ttu-id="73b0b-112">このセルの値は、[**段落**] タブ、[**テキスト**] ダイアログ ボックスで、**方向**の設定に対応して ([**ホーム**] タブで、矢印をクリック、**フォント**) されている場合は、複雑なを使用する言語のスクリプトのテキストを表示します。**Microsoft Office 言語設定**] ダイアログ ボックスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="73b0b-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="73b0b-113">([**スタート**] ボタン [**すべてのプログラム**] をクリックして、 **Microsoft Office**、 **Microsoft Office ツール**] をクリックして、 **Microsoft Office 言語設定**] をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="73b0b-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="73b0b-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Flags] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="73b0b-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73b0b-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="73b0b-115">Cell name:</span></span>  <br/> |<span data-ttu-id="73b0b-116">Para.Flags [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="73b0b-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="73b0b-117">プログラムから、インデックスによって [Flags] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="73b0b-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73b0b-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="73b0b-118">Section index:</span></span>  <br/> |<span data-ttu-id="73b0b-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="73b0b-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="73b0b-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="73b0b-120">Row index:</span></span>  <br/> |<span data-ttu-id="73b0b-121">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="73b0b-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="73b0b-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="73b0b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="73b0b-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="73b0b-123">**visFlags**</span></span> <br/> |
   

