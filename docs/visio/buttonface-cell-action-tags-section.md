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
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337540"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="5c580-103">[ButtonFace] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="5c580-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="5c580-104">アクション タグ ボタンに表示されるボタン イメージの ID を示します。</span><span class="sxs-lookup"><span data-stu-id="5c580-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5c580-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="5c580-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5c580-106">解説</span><span class="sxs-lookup"><span data-stu-id="5c580-106">Remarks</span></span>

<span data-ttu-id="5c580-107">[ButtonFace] セル内の文字列は Microsoft Office のボタン イメージの ID を示します。</span><span class="sxs-lookup"><span data-stu-id="5c580-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="5c580-108">値 0 (ゼロ) または空白は、標準のアクションタグ "i" [情報] ボタンに既定で設定されます。</span><span class="sxs-lookup"><span data-stu-id="5c580-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![標準アクションタグ "i" [情報] ボタン](media/InfoPS_ZA10180114.gif)<span data-ttu-id="5c580-110">.</span><span class="sxs-lookup"><span data-stu-id="5c580-110"></span></span>
  
<span data-ttu-id="5c580-111">[ButtonFace] セルに使用される ID は、 \*\*CommandBarButton \*\* オブジェクトの  \*\*FaceID \*\* プロパティで使用される ID と同じです。</span><span class="sxs-lookup"><span data-stu-id="5c580-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="5c580-112">これらの id の詳細については、MSDN の「コマンドバーボタンイメージを使用する」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="5c580-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="5c580-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ButtonFace] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5c580-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c580-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="5c580-114">Cell name:</span></span>  <br/> | <span data-ttu-id="5c580-115">タグ.</span><span class="sxs-lookup"><span data-stu-id="5c580-115">SmartTags.</span></span>  <span data-ttu-id="5c580-116">*名前*です。SmartTags を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c580-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="5c580-117">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="5c580-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="5c580-118">プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c580-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c580-119">セクション インデックス :</span><span class="sxs-lookup"><span data-stu-id="5c580-119">Section index:</span></span>  <br/> |<span data-ttu-id="5c580-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="5c580-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="5c580-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5c580-121">Row index:</span></span>  <br/> |<span data-ttu-id="5c580-122">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="5c580-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5c580-123">セル インデックス :</span><span class="sxs-lookup"><span data-stu-id="5c580-123">Cell index:</span></span>  <br/> |<span data-ttu-id="5c580-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="5c580-124">**visSmartTagButtonFace**</span></span> <br/> |
   

