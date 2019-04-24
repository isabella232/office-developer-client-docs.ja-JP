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
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346222"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="8a0b0-103">[Flags] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="8a0b0-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="8a0b0-104">テキストの方向が左から右か、右から左かを示します。</span><span class="sxs-lookup"><span data-stu-id="8a0b0-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="8a0b0-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8a0b0-105">**Value**</span></span>|<span data-ttu-id="8a0b0-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8a0b0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a0b0-107">.0</span><span class="sxs-lookup"><span data-stu-id="8a0b0-107">0</span></span>  <br/> |<span data-ttu-id="8a0b0-108">テキストの方向は、左から右です (既定値)。</span><span class="sxs-lookup"><span data-stu-id="8a0b0-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="8a0b0-109">1-d</span><span class="sxs-lookup"><span data-stu-id="8a0b0-109">1</span></span>  <br/> |<span data-ttu-id="8a0b0-110">テキストの方向は、右から左です。</span><span class="sxs-lookup"><span data-stu-id="8a0b0-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a0b0-111">解説</span><span class="sxs-lookup"><span data-stu-id="8a0b0-111">Remarks</span></span>

<span data-ttu-id="8a0b0-112">このセルの値は、[**テキスト**] ダイアログボックスの [段落] タブ ([**ホーム**] タブの [**フォント**] 矢印をクリックすると表示されます) の [**段落**] タブでの**方向**の設定に対応しています。これは、コンプレックススクリプトのテキストを使用する言語が次の場合にのみ表示されます。[ **Microsoft Office 言語設定**] ダイアログボックスに追加されました。</span><span class="sxs-lookup"><span data-stu-id="8a0b0-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="8a0b0-113">([**スタート**]、 **[すべてのプログラム**]、[ **microsoft office**]、[microsoft office**ツール**]、[ **microsoft office の言語設定**] の順にクリックします)。</span><span class="sxs-lookup"><span data-stu-id="8a0b0-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="8a0b0-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Flags] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a0b0-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a0b0-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="8a0b0-115">Cell name:</span></span>  <br/> |<span data-ttu-id="8a0b0-116"><1> [ *i* ]、 *i* =、2、3...</span><span class="sxs-lookup"><span data-stu-id="8a0b0-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8a0b0-117">プログラムから、インデックスによって [Flags] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a0b0-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a0b0-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a0b0-118">Section index:</span></span>  <br/> |<span data-ttu-id="8a0b0-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8a0b0-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="8a0b0-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a0b0-120">Row index:</span></span>  <br/> |<span data-ttu-id="8a0b0-121">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="8a0b0-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8a0b0-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8a0b0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="8a0b0-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="8a0b0-123">**visFlags**</span></span> <br/> |
   

