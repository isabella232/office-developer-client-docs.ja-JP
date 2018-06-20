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
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804948"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="76c1d-103">[BulletString] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="76c1d-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="76c1d-104">箇条書きのスタイルをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="76c1d-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="76c1d-105">注釈</span><span class="sxs-lookup"><span data-stu-id="76c1d-105">Remarks</span></span>

<span data-ttu-id="76c1d-p101">スタイルを引用符で囲み、文字列として入力します。たとえば、"000." のように入力します。</span><span class="sxs-lookup"><span data-stu-id="76c1d-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="76c1d-108">設定することも、このセルの値、図形を右クリックして**形式**、**テキスト**をクリックし、 **[箇条書き**] タブをポイントします。</span><span class="sxs-lookup"><span data-stu-id="76c1d-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="76c1d-109">取得する、[BulletString] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="76c1d-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76c1d-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="76c1d-110">Cell name:</span></span>  <br/> |<span data-ttu-id="76c1d-111">Para.BulletStr [ *i* ]、 *i* = < 1 > では、2、3、.</span><span class="sxs-lookup"><span data-stu-id="76c1d-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="76c1d-112">プログラムから、インデックスによって [BulletString] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="76c1d-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76c1d-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="76c1d-113">Section index:</span></span>  <br/> |<span data-ttu-id="76c1d-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="76c1d-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="76c1d-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="76c1d-115">Row index:</span></span>  <br/> |<span data-ttu-id="76c1d-116">**visRowParagraph** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="76c1d-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="76c1d-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="76c1d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="76c1d-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="76c1d-118">**visBulletString**</span></span> <br/> |
   

