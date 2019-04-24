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
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337612"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="32a31-103">[BulletSize] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="32a31-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="32a31-104">箇条書きのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="32a31-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="32a31-105">解説</span><span class="sxs-lookup"><span data-stu-id="32a31-105">Remarks</span></span>

<span data-ttu-id="32a31-106">この値は、定義済みの箇条書きまたはユーザー設定の箇条書きに対して、パーセントか特定の値のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="32a31-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="32a31-107">値がゼロ (0) の場合、行頭文字は、段落の最初の文字と同じフォントサイズになります。</span><span class="sxs-lookup"><span data-stu-id="32a31-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="32a31-108">値がパーセントの場合、箇条書きは段落の最初の文字に指定したパーセントのフォント サイズになります。</span><span class="sxs-lookup"><span data-stu-id="32a31-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="32a31-109">負の数字はパーセントと見なします。</span><span class="sxs-lookup"><span data-stu-id="32a31-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="32a31-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BulletSize] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="32a31-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32a31-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="32a31-111">Cell name:</span></span>  <br/> | <span data-ttu-id="32a31-112">BulletFontSize [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="32a31-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="32a31-113">プログラムから、インデックスによって [BulletSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="32a31-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32a31-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="32a31-114">Section index:</span></span>  <br/> |<span data-ttu-id="32a31-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="32a31-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="32a31-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="32a31-116">Row index:</span></span>  <br/> |<span data-ttu-id="32a31-117">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="32a31-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="32a31-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="32a31-118">Cell index:</span></span>  <br/> |<span data-ttu-id="32a31-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="32a31-119">**visBulletFontSize**</span></span> <br/> |
   

