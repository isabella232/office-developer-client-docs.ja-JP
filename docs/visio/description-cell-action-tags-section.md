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
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805223"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="a2c6e-103">[Description] セル ([操作タグ] セクション)</span><span class="sxs-lookup"><span data-stu-id="a2c6e-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="a2c6e-104">アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2c6e-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2c6e-105">備考</span><span class="sxs-lookup"><span data-stu-id="a2c6e-105">Remarks</span></span>

<span data-ttu-id="a2c6e-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a2c6e-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2c6e-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="a2c6e-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a2c6e-108">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="a2c6e-108">SmartTags.</span></span>  <span data-ttu-id="a2c6e-109">*名*です。説明するスマート タグ。</span><span class="sxs-lookup"><span data-stu-id="a2c6e-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="a2c6e-110">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="a2c6e-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="a2c6e-111">プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2c6e-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2c6e-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a2c6e-112">Section index:</span></span>  <br/> |<span data-ttu-id="a2c6e-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="a2c6e-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="a2c6e-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a2c6e-114">Row index:</span></span>  <br/> |<span data-ttu-id="a2c6e-115">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="a2c6e-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a2c6e-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a2c6e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a2c6e-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="a2c6e-117">**visSmartTagDescription**</span></span> <br/> |
   

