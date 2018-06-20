---
title: '[AvoidPageBreaks] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80000
localization_priority: Normal
ms.assetid: 7d2ec869-7ffa-3b41-8126-3f4889501e0c
description: 図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。
ms.openlocfilehash: 045ceca430c6c285ad4e454b9d17f9dbd7492a4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804790"
---
# <a name="avoidpagebreaks-cell-page-layout-section"></a><span data-ttu-id="82e36-103">[AvoidPageBreaks] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="82e36-103">AvoidPageBreaks Cell (Page Layout Section)</span></span>

<span data-ttu-id="82e36-104">図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="82e36-104">Determines whether shapes can be placed over page breaks when the shapes are incrementally aligned, incrementally spaced, or both.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82e36-105">備考</span><span class="sxs-lookup"><span data-stu-id="82e36-105">Remarks</span></span>

<span data-ttu-id="82e36-106">参照を取得する AvoidPageBreaks のセルに名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="82e36-106">To get a reference to the AvoidPageBreaks cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82e36-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="82e36-107">Cell name:</span></span>  <br/> |<span data-ttu-id="82e36-108">AvoidPageBreaks</span><span class="sxs-lookup"><span data-stu-id="82e36-108">AvoidPageBreaks</span></span>  <br/> |
   
<span data-ttu-id="82e36-109">プログラムから、インデックスによって [AvoidPageBreaks] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="82e36-109">To get a reference to the AvoidPageBreaks cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82e36-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="82e36-110">Section index:</span></span>  <br/> |<span data-ttu-id="82e36-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="82e36-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="82e36-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="82e36-112">Row index:</span></span>  <br/> |<span data-ttu-id="82e36-113">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="82e36-113">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="82e36-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="82e36-114">Cell index:</span></span>  <br/> |<span data-ttu-id="82e36-115">**visPLOAvoidPageBreaks**</span><span class="sxs-lookup"><span data-stu-id="82e36-115">**visPLOAvoidPageBreaks**</span></span> <br/> |
   

