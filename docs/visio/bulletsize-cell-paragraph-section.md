---
title: '[BulletSize] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: 箇条書きのサイズを指定します。
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804922"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="7009e-103">[BulletSize] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="7009e-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="7009e-104">箇条書きのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="7009e-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7009e-105">備考</span><span class="sxs-lookup"><span data-stu-id="7009e-105">Remarks</span></span>

<span data-ttu-id="7009e-106">この値は、定義済みの箇条書きまたはユーザー設定の箇条書きに対して、パーセントか特定の値のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7009e-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="7009e-107">値がゼロ (0) の場合は、行頭文字は、段落の最初の文字と同じフォント サイズ。</span><span class="sxs-lookup"><span data-stu-id="7009e-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="7009e-108">値がパーセント値の場合は、行頭文字、段落の最初の文字のフォント サイズに対する割合でサイズが。</span><span class="sxs-lookup"><span data-stu-id="7009e-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="7009e-109">負の値は、パーセンテージとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="7009e-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="7009e-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[BulletSize] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7009e-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7009e-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="7009e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7009e-112">Para.BulletFontSize [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="7009e-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7009e-113">プログラムから、インデックスによって [BulletSize] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7009e-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7009e-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7009e-114">Section index:</span></span>  <br/> |<span data-ttu-id="7009e-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7009e-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="7009e-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7009e-116">Row index:</span></span>  <br/> |<span data-ttu-id="7009e-117">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="7009e-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7009e-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7009e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7009e-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="7009e-119">**visBulletFontSize**</span></span> <br/> |
   

