---
title: '[ButtonFace] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: アクション タグ ボタンに表示されるボタン イメージの ID を示します。
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804938"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="ecfeb-103">[ButtonFace] セル ([操作タグ] セクション)</span><span class="sxs-lookup"><span data-stu-id="ecfeb-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="ecfeb-104">アクション タグ ボタンに表示されるボタン イメージの ID を示します。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ecfeb-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ecfeb-106">備考</span><span class="sxs-lookup"><span data-stu-id="ecfeb-106">Remarks</span></span>

<span data-ttu-id="ecfeb-107">ButtonFace] セルに含まれる文字列は、Microsoft Office のボタン イメージの ID を表します。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="ecfeb-108">値が 0 (ゼロ) の標準のアクション タグの"i"情報ボタンの既定値を空白または![](media/InfoPS_ZA10180114.gif)。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button ![](media/InfoPS_ZA10180114.gif).</span></span>
  
<span data-ttu-id="ecfeb-109">ButtonFace] セルに使用できる Id は、 **CommandBarButton**オブジェクトの**FaceID**プロパティで使用される Id と同じです。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="ecfeb-110">これらの Id の詳細については、MSDN の「コマンド バー ボタンのイメージを使用する」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="ecfeb-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ButtonFace] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-111">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecfeb-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="ecfeb-112">Cell name:</span></span>  <br/> | <span data-ttu-id="ecfeb-113">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-113">SmartTags.</span></span>  <span data-ttu-id="ecfeb-114">*名*です。ButtonFace、スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-114">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="ecfeb-115">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="ecfeb-115">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="ecfeb-116">プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ecfeb-116">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecfeb-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ecfeb-117">Section index:</span></span>  <br/> |<span data-ttu-id="ecfeb-118">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="ecfeb-118">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="ecfeb-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ecfeb-119">Row index:</span></span>  <br/> |<span data-ttu-id="ecfeb-120">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="ecfeb-120">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ecfeb-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ecfeb-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ecfeb-122">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="ecfeb-122">**visSmartTagButtonFace**</span></span> <br/> |
   

