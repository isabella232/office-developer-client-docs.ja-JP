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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338193"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="4c325-103">[Bullet] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="4c325-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="4c325-104">箇条書きのスタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="4c325-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="4c325-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4c325-105">**Value**</span></span>|<span data-ttu-id="4c325-106">**箇条書きのスタイル**</span><span class="sxs-lookup"><span data-stu-id="4c325-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c325-107">.0</span><span class="sxs-lookup"><span data-stu-id="4c325-107">0</span></span>  <br/> |<span data-ttu-id="4c325-108">None</span><span class="sxs-lookup"><span data-stu-id="4c325-108">None</span></span>  <br/> |
|<span data-ttu-id="4c325-109">1-d</span><span class="sxs-lookup"><span data-stu-id="4c325-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="4c325-110">pbm-2</span><span class="sxs-lookup"><span data-stu-id="4c325-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="4c325-111">1/3</span><span class="sxs-lookup"><span data-stu-id="4c325-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="4c325-112">2/4</span><span class="sxs-lookup"><span data-stu-id="4c325-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="4c325-113">5</span><span class="sxs-lookup"><span data-stu-id="4c325-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="4c325-114">シックス</span><span class="sxs-lookup"><span data-stu-id="4c325-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="4c325-115">7</span><span class="sxs-lookup"><span data-stu-id="4c325-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="4c325-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c325-116">Section index:</span></span>  <br/> |<span data-ttu-id="4c325-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="4c325-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="4c325-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c325-118">Row index:</span></span>  <br/> |<span data-ttu-id="4c325-119">**visRowParagraph** +  *i* = \*\* 0、1、2、...</span><span class="sxs-lookup"><span data-stu-id="4c325-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="4c325-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4c325-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4c325-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="4c325-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c325-122">解説</span><span class="sxs-lookup"><span data-stu-id="4c325-122">Remarks</span></span>

<span data-ttu-id="4c325-123">このセルの値は、図形を右クリックして [**書式**] をポイントし、[**テキスト**]、[**箇条書き**] の順にクリックして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="4c325-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="4c325-124">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Bullet] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4c325-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c325-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="4c325-125">Cell name:</span></span>  <br/> |<span data-ttu-id="4c325-126">段落記号 [ *i* ] = <1> \*\* 、2、3、...</span><span class="sxs-lookup"><span data-stu-id="4c325-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="4c325-127">プログラムから、インデックスによって [Bullet] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c325-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

