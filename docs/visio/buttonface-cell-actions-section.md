---
title: '[ButtonFace] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407376"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="b84da-103">[ButtonFace] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="b84da-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="b84da-104">ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。</span><span class="sxs-lookup"><span data-stu-id="b84da-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b84da-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="b84da-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b84da-106">注釈</span><span class="sxs-lookup"><span data-stu-id="b84da-106">Remarks</span></span>

<span data-ttu-id="b84da-p101">[ButtonFace] セルに含まれる文字列は Microsoft Office のボタン イメージの ID を表します。値ゼロ (0) または空白は、アイコンが表示されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b84da-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="b84da-109">[ButtonFace] セルに使用される ID は、 **CommandBarButton** オブジェクトの  **FaceID** プロパティで使用される ID と同じです。</span><span class="sxs-lookup"><span data-stu-id="b84da-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="b84da-110">これらの ID の詳細については、MSDN で "コマンド バー ボタンイメージを操作する" を検索します。</span><span class="sxs-lookup"><span data-stu-id="b84da-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="b84da-111">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [ButtonFace] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b84da-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b84da-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="b84da-112">Cell name:</span></span>  <br/> |<span data-ttu-id="b84da-113">**アクション**。</span><span class="sxs-lookup"><span data-stu-id="b84da-113">**Actions**.</span></span>  <span data-ttu-id="b84da-114">*name*  .</span><span class="sxs-lookup"><span data-stu-id="b84da-114">*name*  .</span></span> <span data-ttu-id="b84da-115">**ButtonFace**         where **Actions**.</span><span class="sxs-lookup"><span data-stu-id="b84da-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="b84da-116">*name*  はアクション行の名前です。</span><span class="sxs-lookup"><span data-stu-id="b84da-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="b84da-117">プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b84da-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b84da-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b84da-118">Section index:</span></span>  <br/> |<span data-ttu-id="b84da-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="b84da-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="b84da-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b84da-120">Row index:</span></span>  <br/> |<span data-ttu-id="b84da-121">**visRowAction**  +  *i* **=** 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b84da-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b84da-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b84da-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b84da-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="b84da-123">**visActionButtonFace**</span></span> <br/> |
   

