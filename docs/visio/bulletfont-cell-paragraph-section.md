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
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438464"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="95dbc-103">[BulletFont] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="95dbc-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="95dbc-104">ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。</span><span class="sxs-lookup"><span data-stu-id="95dbc-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="95dbc-105">注釈</span><span class="sxs-lookup"><span data-stu-id="95dbc-105">Remarks</span></span>

<span data-ttu-id="95dbc-p101">フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。値が 0 でユーザー設定の箇条書き文字列がある場合、使用されるフォントは、段落の最初の文字のフォントと同じです。</span><span class="sxs-lookup"><span data-stu-id="95dbc-p101">Font numbers vary according to the fonts installed on your system. If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="95dbc-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BulletFont] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95dbc-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95dbc-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="95dbc-109">Cell name:</span></span>  <br/> | <span data-ttu-id="95dbc-110">Para.BulletFont[ i ]*ここで\*\*、i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="95dbc-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95dbc-111">プログラムから、インデックスによって [BulletFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="95dbc-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95dbc-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="95dbc-112">Section index:</span></span>  <br/> |<span data-ttu-id="95dbc-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="95dbc-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="95dbc-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="95dbc-114">Row index:</span></span>  <br/> |<span data-ttu-id="95dbc-115">**visRowParagraph**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="95dbc-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="95dbc-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="95dbc-116">Cell index:</span></span>  <br/> |<span data-ttu-id="95dbc-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="95dbc-117">**visBulletFont**</span></span> <br/> |
   

