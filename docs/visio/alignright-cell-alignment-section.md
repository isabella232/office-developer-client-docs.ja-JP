---
title: '[AlignRight] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251297
localization_priority: Normal
ms.assetid: c6d298a4-1602-a53c-bb5d-2ef16b43f722
description: 親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
ms.openlocfilehash: 8bb3f68a9b7e6fb08cbd95ee0240e35f519d4fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804775"
---
# <a name="alignright-cell-alignment-section"></a><span data-ttu-id="1dcf4-103">[AlignRight] セル ([配置] セクション)</span><span class="sxs-lookup"><span data-stu-id="1dcf4-103">AlignRight Cell (Alignment Section)</span></span>

<span data-ttu-id="1dcf4-104">親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="1dcf4-104">Determines the horizontal position, relative to the origin of its parent, of a vertical guide or guide point to which the shape's right border is aligned.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1dcf4-105">備考</span><span class="sxs-lookup"><span data-stu-id="1dcf4-105">Remarks</span></span>

<span data-ttu-id="1dcf4-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignRight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1dcf4-106">To get a reference to the AlignRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dcf4-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="1dcf4-107">Cell name:</span></span>  <br/> | <span data-ttu-id="1dcf4-108">AlignRight</span><span class="sxs-lookup"><span data-stu-id="1dcf4-108">AlignRight</span></span>  <br/> |
   
<span data-ttu-id="1dcf4-109">プログラムから、インデックスによって [AlignRight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1dcf4-109">To get a reference to the AlignRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dcf4-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-110">Section index:</span></span>  <br/> |<span data-ttu-id="1dcf4-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1dcf4-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1dcf4-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-112">Row index:</span></span>  <br/> |<span data-ttu-id="1dcf4-113">**visRowAlign**</span><span class="sxs-lookup"><span data-stu-id="1dcf4-113">**visRowAlign**</span></span> <br/> |
| <span data-ttu-id="1dcf4-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-114">Cell index:</span></span>  <br/> |<span data-ttu-id="1dcf4-115">**visAlignRight**</span><span class="sxs-lookup"><span data-stu-id="1dcf4-115">**visAlignRight**</span></span> <br/> |
   

