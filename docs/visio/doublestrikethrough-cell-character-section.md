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
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360593"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="0d813-103">[DoubleStrikethrough] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="0d813-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="0d813-104">テキストを二重取り消し線で書式設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0d813-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d813-105">解説</span><span class="sxs-lookup"><span data-stu-id="0d813-105">Remarks</span></span>

<span data-ttu-id="0d813-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DoubleStrikethrough] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d813-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d813-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0d813-107">Cell name:</span></span>  <br/> | <span data-ttu-id="0d813-108">[doublestrikethrough] [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="0d813-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0d813-109">プログラムから、インデックスによって [DoubleStrikethrough] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d813-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d813-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d813-110">Section index:</span></span>  <br/> |<span data-ttu-id="0d813-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="0d813-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="0d813-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d813-112">Row index:</span></span>  <br/> |<span data-ttu-id="0d813-113">**visRowCharacter** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="0d813-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0d813-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d813-114">Cell index:</span></span>  <br/> |<span data-ttu-id="0d813-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="0d813-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

