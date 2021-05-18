---
title: '[Bullet] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: 箇条書きのスタイルを指定します。
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422769"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="fcb93-103">[Bullet] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="fcb93-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="fcb93-104">箇条書きのスタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="fcb93-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="fcb93-105">**値**</span><span class="sxs-lookup"><span data-stu-id="fcb93-105">**Value**</span></span>|<span data-ttu-id="fcb93-106">**箇条書きスタイル**</span><span class="sxs-lookup"><span data-stu-id="fcb93-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcb93-107">0</span><span class="sxs-lookup"><span data-stu-id="fcb93-107">0</span></span>  <br/> |<span data-ttu-id="fcb93-108">None</span><span class="sxs-lookup"><span data-stu-id="fcb93-108">None</span></span>  <br/> |
|<span data-ttu-id="fcb93-109">1</span><span class="sxs-lookup"><span data-stu-id="fcb93-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="fcb93-110">2</span><span class="sxs-lookup"><span data-stu-id="fcb93-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="fcb93-111">3</span><span class="sxs-lookup"><span data-stu-id="fcb93-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="fcb93-112">4</span><span class="sxs-lookup"><span data-stu-id="fcb93-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="fcb93-113">5</span><span class="sxs-lookup"><span data-stu-id="fcb93-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="fcb93-114">6</span><span class="sxs-lookup"><span data-stu-id="fcb93-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="fcb93-115">7</span><span class="sxs-lookup"><span data-stu-id="fcb93-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="fcb93-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcb93-116">Section index:</span></span>  <br/> |<span data-ttu-id="fcb93-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="fcb93-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="fcb93-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcb93-118">Row index:</span></span>  <br/> |<span data-ttu-id="fcb93-119">**visRowParagraph**  +  *i* *=* 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="fcb93-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="fcb93-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fcb93-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fcb93-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="fcb93-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcb93-122">注釈</span><span class="sxs-lookup"><span data-stu-id="fcb93-122">Remarks</span></span>

<span data-ttu-id="fcb93-123">このセルの値は、図形を右クリックして [**書式**] をポイントし、[**テキスト**]、[**箇条書き**] の順にクリックして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="fcb93-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="fcb93-124">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Bullet] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fcb93-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcb93-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="fcb93-125">Cell name:</span></span>  <br/> |<span data-ttu-id="fcb93-126">Para.Bullet[ *i*  ] ここで  *、i*  = <1>、2、3、..</span><span class="sxs-lookup"><span data-stu-id="fcb93-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="fcb93-127">プログラムから、インデックスによって [Bullet] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fcb93-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

