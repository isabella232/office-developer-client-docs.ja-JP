---
title: '[TxtPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: Y の決定に、テキスト ブロックの図形の原点を基準として回転の中心の座標。 既定の数式は次のとおりです。
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806707"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="81f24-104">[TxtPinY] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="81f24-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="81f24-105">*Y*の決定に、テキスト ブロックの図形の原点を基準として回転の中心の座標。</span><span class="sxs-lookup"><span data-stu-id="81f24-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="81f24-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="81f24-106">The default formula is:</span></span> 
  
<span data-ttu-id="81f24-107">= 高さ\*0.5</span><span class="sxs-lookup"><span data-stu-id="81f24-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81f24-108">備考</span><span class="sxs-lookup"><span data-stu-id="81f24-108">Remarks</span></span>

<span data-ttu-id="81f24-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [txtpiny] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="81f24-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81f24-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="81f24-110">Cell name:</span></span>  <br/> | <span data-ttu-id="81f24-111">[Txtpiny]</span><span class="sxs-lookup"><span data-stu-id="81f24-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="81f24-112">プログラムから、インデックスによって [txtpiny] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="81f24-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81f24-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="81f24-113">Section index:</span></span>  <br/> |<span data-ttu-id="81f24-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81f24-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="81f24-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="81f24-115">Row index:</span></span>  <br/> |<span data-ttu-id="81f24-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="81f24-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="81f24-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="81f24-117">Cell index:</span></span>  <br/> |<span data-ttu-id="81f24-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="81f24-118">**visXFormPinY**</span></span> <br/> |
   

