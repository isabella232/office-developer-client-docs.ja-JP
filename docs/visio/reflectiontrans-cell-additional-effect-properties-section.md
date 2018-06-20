---
title: '[ReflectionTrans] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1d155af5-b809-4367-b093-1218a1597656
description: 0 から 100% の割合として、反射の透明度を決定します。
ms.openlocfilehash: 31f39a19313f1f1622282ea0704694bd612ef55f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806162"
---
# <a name="reflectiontrans-cell-additional-effect-properties-section"></a><span data-ttu-id="a08dc-103">[ReflectionTrans] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="a08dc-103">ReflectionTrans Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="a08dc-104">0 から 100% の割合として、反射の透明度を決定します。</span><span class="sxs-lookup"><span data-stu-id="a08dc-104">Determines the transparency of the reflection, as a percentage from 0 to 100%.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a08dc-105">備考</span><span class="sxs-lookup"><span data-stu-id="a08dc-105">Remarks</span></span>

<span data-ttu-id="a08dc-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReflectionTrans** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a08dc-106">To get a reference to the **ReflectionTrans** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a08dc-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="a08dc-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a08dc-108">ReflectionTrans</span><span class="sxs-lookup"><span data-stu-id="a08dc-108">ReflectionTrans</span></span>  <br/> |
   
<span data-ttu-id="a08dc-109">プログラムから、インデックスによって [ **ReflectionTrans** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a08dc-109">To get a reference to the **ReflectionTrans** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a08dc-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a08dc-110">Section index:</span></span>  <br/> |<span data-ttu-id="a08dc-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a08dc-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a08dc-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a08dc-112">Row index:</span></span>  <br/> |<span data-ttu-id="a08dc-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="a08dc-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="a08dc-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a08dc-114">Cell index:</span></span>  <br/> |<span data-ttu-id="a08dc-115">**visReflectionTrans**</span><span class="sxs-lookup"><span data-stu-id="a08dc-115">**visReflectionTrans**</span></span> <br/> |
   

