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
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804941"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="b21a4-103">[Bullet] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="b21a4-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="b21a4-104">箇条書きのスタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b21a4-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="b21a4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b21a4-105">**Value**</span></span>|<span data-ttu-id="b21a4-106">**箇条書きのスタイル**</span><span class="sxs-lookup"><span data-stu-id="b21a4-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b21a4-107">0</span><span class="sxs-lookup"><span data-stu-id="b21a4-107">0</span></span>  <br/> |<span data-ttu-id="b21a4-108">なし</span><span class="sxs-lookup"><span data-stu-id="b21a4-108">None</span></span>  <br/> |
|<span data-ttu-id="b21a4-109">1</span><span class="sxs-lookup"><span data-stu-id="b21a4-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="b21a4-110">2</span><span class="sxs-lookup"><span data-stu-id="b21a4-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="b21a4-111">3</span><span class="sxs-lookup"><span data-stu-id="b21a4-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="b21a4-112">4</span><span class="sxs-lookup"><span data-stu-id="b21a4-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="b21a4-113">5</span><span class="sxs-lookup"><span data-stu-id="b21a4-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="b21a4-114">6</span><span class="sxs-lookup"><span data-stu-id="b21a4-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="b21a4-115">7</span><span class="sxs-lookup"><span data-stu-id="b21a4-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="b21a4-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b21a4-116">Section index:</span></span>  <br/> |<span data-ttu-id="b21a4-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="b21a4-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="b21a4-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b21a4-118">Row index:</span></span>  <br/> |<span data-ttu-id="b21a4-119">**visRowParagraph** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="b21a4-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="b21a4-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b21a4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b21a4-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="b21a4-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b21a4-122">備考</span><span class="sxs-lookup"><span data-stu-id="b21a4-122">Remarks</span></span>

<span data-ttu-id="b21a4-123">設定することも、このセルの値、図形を右クリックして**形式**、**テキスト**をクリックし、 **[箇条書き**] タブをポイントします。</span><span class="sxs-lookup"><span data-stu-id="b21a4-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="b21a4-124">取得する、[Bullet] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b21a4-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b21a4-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="b21a4-125">Cell name:</span></span>  <br/> |<span data-ttu-id="b21a4-126">Para.Bullet [ *i* ]、 *i* = < 1 > では、2、3、.</span><span class="sxs-lookup"><span data-stu-id="b21a4-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="b21a4-127">プログラムから、インデックスによって [Bullet] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b21a4-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

