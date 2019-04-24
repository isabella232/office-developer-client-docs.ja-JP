---
title: '[Description] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360232"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="96379-103">[Description] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="96379-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="96379-104">アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="96379-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96379-105">解説</span><span class="sxs-lookup"><span data-stu-id="96379-105">Remarks</span></span>

<span data-ttu-id="96379-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="96379-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96379-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="96379-107">Cell name:</span></span>  <br/> | <span data-ttu-id="96379-108">タグ.</span><span class="sxs-lookup"><span data-stu-id="96379-108">SmartTags.</span></span>  <span data-ttu-id="96379-109">*名前*です。SmartTags の説明。</span><span class="sxs-lookup"><span data-stu-id="96379-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="96379-110">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="96379-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="96379-111">プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="96379-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96379-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="96379-112">Section index:</span></span>  <br/> |<span data-ttu-id="96379-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="96379-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="96379-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="96379-114">Row index:</span></span>  <br/> |<span data-ttu-id="96379-115">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="96379-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="96379-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="96379-116">Cell index:</span></span>  <br/> |<span data-ttu-id="96379-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="96379-117">**visSmartTagDescription**</span></span> <br/> |
   

