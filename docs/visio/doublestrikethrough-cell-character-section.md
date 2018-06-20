---
title: '[DoubleStrikethrough] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: テキストを二重取り消し線で書式設定するかどうかを指定します。
ms.openlocfilehash: dcd7c7769da8298c1f6ab474d2b63fc982f479b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805278"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="80bbe-103">[DoubleStrikethrough] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="80bbe-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="80bbe-104">テキストを二重取り消し線で書式設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="80bbe-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80bbe-105">備考</span><span class="sxs-lookup"><span data-stu-id="80bbe-105">Remarks</span></span>

<span data-ttu-id="80bbe-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DoubleStrikethrough] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="80bbe-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80bbe-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="80bbe-107">Cell name:</span></span>  <br/> | <span data-ttu-id="80bbe-108">Char.DoubleStrikethrough [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="80bbe-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="80bbe-109">プログラムから、インデックスによって [DoubleStrikethrough] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="80bbe-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80bbe-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="80bbe-110">Section index:</span></span>  <br/> |<span data-ttu-id="80bbe-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="80bbe-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="80bbe-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="80bbe-112">Row index:</span></span>  <br/> |<span data-ttu-id="80bbe-113">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="80bbe-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="80bbe-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="80bbe-114">Cell index:</span></span>  <br/> |<span data-ttu-id="80bbe-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="80bbe-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

