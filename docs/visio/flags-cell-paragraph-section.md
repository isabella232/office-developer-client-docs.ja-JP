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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413116"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="4c053-103">[Flags] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="4c053-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="4c053-104">テキストの方向が左から右か、右から左かを示します。</span><span class="sxs-lookup"><span data-stu-id="4c053-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="4c053-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4c053-105">**Value**</span></span>|<span data-ttu-id="4c053-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="4c053-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c053-107">0</span><span class="sxs-lookup"><span data-stu-id="4c053-107">0</span></span>  <br/> |<span data-ttu-id="4c053-108">テキストの方向は、左から右です (既定値)。</span><span class="sxs-lookup"><span data-stu-id="4c053-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="4c053-109">1</span><span class="sxs-lookup"><span data-stu-id="4c053-109">1</span></span>  <br/> |<span data-ttu-id="4c053-110">テキストの方向は、右から左です。</span><span class="sxs-lookup"><span data-stu-id="4c053-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c053-111">注釈</span><span class="sxs-lookup"><span data-stu-id="4c053-111">Remarks</span></span>

<span data-ttu-id="4c053-112">このセルの値は、[テキスト]ダイアログ ボックスの [段落]タブの [方向] 設定に対応します ([ホーム] タブの [フォント] 矢印をクリックします)。これは、**複雑** なスクリプト テキストを使用する言語が Microsoft Office の [言語の基本設定] ダイアログ ボックスに追加されている場合にのみ表示されます。  </span><span class="sxs-lookup"><span data-stu-id="4c053-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="4c053-113">([**スタート] ボタン**、[すべてのプログラム **]** の順にクリックし、[Microsoft Office]**をクリック** し、[Microsoft Office **ツール**] をクリックし、[言語の基本設定] をMicrosoft Office **クリック** します。</span><span class="sxs-lookup"><span data-stu-id="4c053-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="4c053-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Flags] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4c053-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c053-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="4c053-115">Cell name:</span></span>  <br/> |<span data-ttu-id="4c053-116">Para.Flags[ *i*  ] ここで  *、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="4c053-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4c053-117">プログラムから、インデックスによって [Flags] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c053-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c053-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c053-118">Section index:</span></span>  <br/> |<span data-ttu-id="4c053-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="4c053-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="4c053-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c053-120">Row index:</span></span>  <br/> |<span data-ttu-id="4c053-121">**visRowParagraph**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4c053-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4c053-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c053-122">Cell index:</span></span>  <br/> |<span data-ttu-id="4c053-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="4c053-123">**visFlags**</span></span> <br/> |
   

