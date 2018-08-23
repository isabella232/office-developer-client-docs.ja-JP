---
title: '[HideForApply] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Microsoft Visio ユーザー インターフェイスのスタイルを表示する場所を決定します。
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805541"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="9fead-103">[HideForApply] セル ([スタイルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="9fead-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="9fead-104">Microsoft Visio ユーザー インターフェイスのスタイルを表示する場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="9fead-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="9fead-105">**値**</span><span class="sxs-lookup"><span data-stu-id="9fead-105">**Value**</span></span>|<span data-ttu-id="9fead-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="9fead-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9fead-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9fead-107">TRUE</span></span>  <br/> | <span data-ttu-id="9fead-108">
          [**ドローイング エクスプローラー**] だけにスタイルを表示します。
</span><span class="sxs-lookup"><span data-stu-id="9fead-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="9fead-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9fead-109">FALSE</span></span>  <br/> | <span data-ttu-id="9fead-110">
          [**ドローイング エクスプローラー**] にスタイルを表示します。
</span><span class="sxs-lookup"><span data-stu-id="9fead-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fead-111">備考</span><span class="sxs-lookup"><span data-stu-id="9fead-111">Remarks</span></span>

<span data-ttu-id="9fead-112">表示されていないスタイルに基づいて新しいスタイルを作成する場合は、この属性は継承されません。</span><span class="sxs-lookup"><span data-stu-id="9fead-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="9fead-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [HideForApply] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9fead-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fead-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="9fead-114">Cell name:</span></span>  <br/> | <span data-ttu-id="9fead-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="9fead-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="9fead-116">プログラムから、インデックスによって [HideForApply] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9fead-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fead-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fead-117">Section index:</span></span>  <br/> |<span data-ttu-id="9fead-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9fead-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9fead-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fead-119">Row index:</span></span>  <br/> |<span data-ttu-id="9fead-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="9fead-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="9fead-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fead-121">Cell index:</span></span>  <br/> |<span data-ttu-id="9fead-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="9fead-122">**visStyleHidden**</span></span> <br/> |
   

