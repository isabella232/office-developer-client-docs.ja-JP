---
title: '[LocalizeMerge] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: 図形を図面間でコピーするときにローカライズするかどうかを指定します。
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805730"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="1f658-103">[LocalizeMerge] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="1f658-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="1f658-104">図形を図面間でコピーするときにローカライズするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="1f658-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="1f658-105">**値**</span><span class="sxs-lookup"><span data-stu-id="1f658-105">**Value**</span></span>|<span data-ttu-id="1f658-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="1f658-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1f658-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1f658-107">TRUE</span></span>  <br/> | <span data-ttu-id="1f658-108">コピー先図面の言語に図形をローカライズします。</span><span class="sxs-lookup"><span data-stu-id="1f658-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="1f658-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1f658-109">FALSE</span></span>  <br/> | <span data-ttu-id="1f658-110">(既定値) のコピー先の文書の言語に基づく図形のローカライズの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1f658-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f658-111">備考</span><span class="sxs-lookup"><span data-stu-id="1f658-111">Remarks</span></span>

<span data-ttu-id="1f658-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LocalizeMerge] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="1f658-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f658-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="1f658-113">Cell name:</span></span>  <br/> | <span data-ttu-id="1f658-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="1f658-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="1f658-115">プログラムから、インデックスによって [LocalizeMerge] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1f658-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f658-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1f658-116">Section index:</span></span>  <br/> |<span data-ttu-id="1f658-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f658-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1f658-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1f658-118">Row index:</span></span>  <br/> |<span data-ttu-id="1f658-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="1f658-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="1f658-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1f658-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1f658-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="1f658-121">**visObjLocalizeMerge**</span></span> <br/> |
   

