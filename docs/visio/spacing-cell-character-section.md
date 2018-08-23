---
title: '[Spacing] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: 複数の文字間の間隔を制御します。間隔は、1/20 ポイント単位で増減できます。
ms.openlocfilehash: ee714306e22cafb7f6d805851a6f977e93172377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806552"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="d2736-104">[Spacing] セル ([文字] セクション)</span><span class="sxs-lookup"><span data-stu-id="d2736-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="d2736-p102">複数の文字間の間隔を制御します。間隔は、1/20 ポイント単位で増減できます。</span><span class="sxs-lookup"><span data-stu-id="d2736-p102">Controls the amount of space between two or more characters. Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2736-107">注釈</span><span class="sxs-lookup"><span data-stu-id="d2736-107">Remarks</span></span>

<span data-ttu-id="d2736-108">このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="d2736-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="d2736-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Spacing] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2736-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2736-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="d2736-110">Cell name:</span></span>  <br/> |<span data-ttu-id="d2736-111">Char.Letterspace [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="d2736-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d2736-112">プログラムから、インデックスによって [Spacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2736-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2736-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2736-113">Section index:</span></span>  <br/> |<span data-ttu-id="d2736-114">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d2736-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d2736-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2736-115">Row index:</span></span>  <br/> |<span data-ttu-id="d2736-116">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="d2736-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d2736-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2736-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d2736-118">**visCharacterLetterspace**</span><span class="sxs-lookup"><span data-stu-id="d2736-118">**visCharacterLetterspace**</span></span> <br/> |
   

