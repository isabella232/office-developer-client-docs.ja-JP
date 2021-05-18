---
title: '[ReflectionBlur] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece15159-6a33-4abd-8775-6fbe1cc43793
description: 図形の反射のぼかしの量を 0.0 ~ 100.0 のポイントで指定します。
ms.openlocfilehash: 67ed06d764b90afbc47895c4c714fefadbe6f062
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408013"
---
# <a name="reflectionblur-cell-additional-effect-properties-section"></a><span data-ttu-id="98c0c-103">[ReflectionBlur] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="98c0c-103">ReflectionBlur Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="98c0c-104">図形の反射のぼかしの量を 0.0 ~ 100.0 のポイントで指定します。</span><span class="sxs-lookup"><span data-stu-id="98c0c-104">Determines the amount of blur for a reflection on a shape, in points between 0.0 and 100.0.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98c0c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="98c0c-105">Remarks</span></span>

<span data-ttu-id="98c0c-106">別の数式 **、Cell** 要素 **の N** 属性の値、または CellsU プロパティを使用したプログラムから、名前によって **ReflectionBlur** セルへの参照を取得するには、次の値を **使用** します。</span><span class="sxs-lookup"><span data-stu-id="98c0c-106">To get a reference to the **ReflectionBlur** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="98c0c-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="98c0c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="98c0c-108">ReflectionBlur</span><span class="sxs-lookup"><span data-stu-id="98c0c-108">ReflectionBlur</span></span>  <br/> |
   
<span data-ttu-id="98c0c-109">プログラムからインデックスによって **ReflectionBlur** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="98c0c-109">To get a reference to the **ReflectionBlur** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="98c0c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="98c0c-110">Section index:</span></span>  <br/> |<span data-ttu-id="98c0c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="98c0c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="98c0c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="98c0c-112">Row index:</span></span>  <br/> |<span data-ttu-id="98c0c-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="98c0c-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="98c0c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="98c0c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="98c0c-115">**visReflectionBlur**</span><span class="sxs-lookup"><span data-stu-id="98c0c-115">**visReflectionBlur**</span></span> <br/> |
   

