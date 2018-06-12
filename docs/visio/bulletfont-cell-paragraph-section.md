---
title: '[BulletFont] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。
ms.openlocfilehash: 7cd3333afc30d30ea7b0e5d35650681074744235
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804950"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="4177e-103">[BulletFont] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="4177e-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="4177e-104">ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。</span><span class="sxs-lookup"><span data-stu-id="4177e-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4177e-105">備考</span><span class="sxs-lookup"><span data-stu-id="4177e-105">Remarks</span></span>

<span data-ttu-id="4177e-p101">フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。値が 0 でユーザー設定の箇条書き文字列がある場合、使用されるフォントは、段落の最初の文字のフォントと同じです。</span><span class="sxs-lookup"><span data-stu-id="4177e-p101">Font numbers vary according to the fonts installed on your system. If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="4177e-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[BulletFont] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4177e-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4177e-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="4177e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4177e-110">Para.BulletFont [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="4177e-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4177e-111">プログラムから、インデックスによって [BulletFont] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4177e-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4177e-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4177e-112">Section index:</span></span>  <br/> |<span data-ttu-id="4177e-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="4177e-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="4177e-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4177e-114">Row index:</span></span>  <br/> |<span data-ttu-id="4177e-115">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="4177e-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4177e-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4177e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="4177e-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="4177e-117">**visBulletFont**</span></span> <br/> |
   

