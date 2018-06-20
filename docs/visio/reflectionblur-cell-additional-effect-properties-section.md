---
title: '[ReflectionBlur] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece15159-6a33-4abd-8775-6fbe1cc43793
description: 0.0 から 100.0 までのポイント単位で、図形上の反射のぼかしの量を決定します。
ms.openlocfilehash: d283531cc10b7a18952dcef398acf050c91bafb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806166"
---
# <a name="reflectionblur-cell-additional-effect-properties-section"></a><span data-ttu-id="7dd43-103">[ReflectionBlur] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="7dd43-103">ReflectionBlur Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="7dd43-104">0.0 から 100.0 までのポイント単位で、図形上の反射のぼかしの量を決定します。</span><span class="sxs-lookup"><span data-stu-id="7dd43-104">Determines the amount of blur for a reflection on a shape, in points between 0.0 and 100.0.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7dd43-105">備考</span><span class="sxs-lookup"><span data-stu-id="7dd43-105">Remarks</span></span>

<span data-ttu-id="7dd43-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReflectionBlur** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7dd43-106">To get a reference to the **ReflectionBlur** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dd43-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="7dd43-107">Cell name:</span></span>  <br/> | <span data-ttu-id="7dd43-108">ReflectionBlur</span><span class="sxs-lookup"><span data-stu-id="7dd43-108">ReflectionBlur</span></span>  <br/> |
   
<span data-ttu-id="7dd43-109">プログラムから、インデックスによって [ **ReflectionBlur** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7dd43-109">To get a reference to the **ReflectionBlur** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dd43-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7dd43-110">Section index:</span></span>  <br/> |<span data-ttu-id="7dd43-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7dd43-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7dd43-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7dd43-112">Row index:</span></span>  <br/> |<span data-ttu-id="7dd43-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="7dd43-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="7dd43-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7dd43-114">Cell index:</span></span>  <br/> |<span data-ttu-id="7dd43-115">**visReflectionBlur**</span><span class="sxs-lookup"><span data-stu-id="7dd43-115">**visReflectionBlur**</span></span> <br/> |
   

