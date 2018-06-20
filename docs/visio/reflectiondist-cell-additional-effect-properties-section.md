---
title: '[ReflectionDist] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 858a3191-420a-4065-9180-ebd8503d1eef
description: 距離の決定に 100.0 0.0 からポイントに、図形から反射をオフセットします。
ms.openlocfilehash: 35cbafdf3bde350fb20035228646a3f65b49e141
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806158"
---
# <a name="reflectiondist-cell-additional-effect-properties-section"></a><span data-ttu-id="8fd9d-103">[ReflectionDist] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="8fd9d-103">ReflectionDist Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="8fd9d-104">距離の決定に 100.0 0.0 からポイントに、図形から反射をオフセットします。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-104">Determines the distance that a reflection is offset from a shape, in points from 0.0 to 100.0.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8fd9d-105">備考</span><span class="sxs-lookup"><span data-stu-id="8fd9d-105">Remarks</span></span>

<span data-ttu-id="8fd9d-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReflectionDist** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-106">To get a reference to the **ReflectionDist** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8fd9d-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="8fd9d-107">Cell name:</span></span>  <br/> | <span data-ttu-id="8fd9d-108">ReflectionDist</span><span class="sxs-lookup"><span data-stu-id="8fd9d-108">ReflectionDist</span></span>  <br/> |
   
<span data-ttu-id="8fd9d-109">プログラムから、インデックスによって [ **ReflectionDist** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-109">To get a reference to the **ReflectionDist** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8fd9d-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8fd9d-110">Section index:</span></span>  <br/> |<span data-ttu-id="8fd9d-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8fd9d-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8fd9d-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8fd9d-112">Row index:</span></span>  <br/> |<span data-ttu-id="8fd9d-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="8fd9d-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="8fd9d-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8fd9d-114">Cell index:</span></span>  <br/> |<span data-ttu-id="8fd9d-115">**visReflectionDist**</span><span class="sxs-lookup"><span data-stu-id="8fd9d-115">**visReflectionDist**</span></span> <br/> |
   

