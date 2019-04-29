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
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405675"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="5b9a5-103">[LocalizeMerge] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="5b9a5-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5b9a5-104">図形を図面間でコピーするときにローカライズするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="5b9a5-105">**値**</span><span class="sxs-lookup"><span data-stu-id="5b9a5-105">**Value**</span></span>|<span data-ttu-id="5b9a5-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b9a5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5b9a5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5b9a5-107">TRUE</span></span>  <br/> | <span data-ttu-id="5b9a5-108">コピー先図面の言語に図形をローカライズします。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="5b9a5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5b9a5-109">FALSE</span></span>  <br/> | <span data-ttu-id="5b9a5-110">コピー先の文書の言語に基づいて図形をローカライズしないようにします (既定値)。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b9a5-111">注釈</span><span class="sxs-lookup"><span data-stu-id="5b9a5-111">Remarks</span></span>

<span data-ttu-id="5b9a5-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocalizeMerge] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b9a5-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="5b9a5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5b9a5-114">[localizemerge]</span><span class="sxs-lookup"><span data-stu-id="5b9a5-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="5b9a5-115">プログラムから、インデックスによって [LocalizeMerge] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b9a5-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5b9a5-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b9a5-116">Section index:</span></span>  <br/> |<span data-ttu-id="5b9a5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5b9a5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5b9a5-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b9a5-118">Row index:</span></span>  <br/> |<span data-ttu-id="5b9a5-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="5b9a5-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="5b9a5-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b9a5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5b9a5-121">**visobjlocalizemerge**</span><span class="sxs-lookup"><span data-stu-id="5b9a5-121">**visObjLocalizeMerge**</span></span> <br/> |
   

