---
title: '[BulletString] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: 箇条書きのスタイルをカスタマイズできます。
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337563"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="81b1d-103">[BulletString] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="81b1d-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="81b1d-104">箇条書きのスタイルをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="81b1d-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81b1d-105">解説</span><span class="sxs-lookup"><span data-stu-id="81b1d-105">Remarks</span></span>

<span data-ttu-id="81b1d-p101">スタイルを引用符で囲み、文字列として入力します。たとえば、"000." のように入力します。</span><span class="sxs-lookup"><span data-stu-id="81b1d-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="81b1d-108">このセルの値は、図形を右クリックして [**書式**] をポイントし、[**テキスト**]、[**箇条書き**] の順にクリックして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="81b1d-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="81b1d-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BulletString] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="81b1d-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81b1d-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="81b1d-110">Cell name:</span></span>  <br/> |<span data-ttu-id="81b1d-111">BulletStr [ *i* ] *i* = <1>、2、3、...</span><span class="sxs-lookup"><span data-stu-id="81b1d-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="81b1d-112">プログラムから、インデックスによって [BulletString] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="81b1d-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81b1d-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="81b1d-113">Section index:</span></span>  <br/> |<span data-ttu-id="81b1d-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="81b1d-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="81b1d-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="81b1d-115">Row index:</span></span>  <br/> |<span data-ttu-id="81b1d-116">**visRowParagraph** +  *i* = \*\* 0、1、2、...</span><span class="sxs-lookup"><span data-stu-id="81b1d-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="81b1d-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="81b1d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="81b1d-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="81b1d-118">**visBulletString**</span></span> <br/> |
   

