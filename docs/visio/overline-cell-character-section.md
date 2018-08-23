---
title: '[Overline] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: テキストの上に線を描画するかどうかを指定します。
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805946"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="c313b-103">[Overline] セル ([文字] セクション)</span><span class="sxs-lookup"><span data-stu-id="c313b-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="c313b-104">テキストの上に線を描画するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c313b-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="c313b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c313b-105">**Value**</span></span>|<span data-ttu-id="c313b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c313b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c313b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c313b-107">TRUE</span></span>  <br/> |<span data-ttu-id="c313b-108">テキストの上に線を描画します。</span><span class="sxs-lookup"><span data-stu-id="c313b-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="c313b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c313b-109">FALSE</span></span>  <br/> |<span data-ttu-id="c313b-110">テキストの上に線を描画しません。</span><span class="sxs-lookup"><span data-stu-id="c313b-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c313b-111">注釈</span><span class="sxs-lookup"><span data-stu-id="c313b-111">Remarks</span></span>

<span data-ttu-id="c313b-112">このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="c313b-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="c313b-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Overline] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c313b-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c313b-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="c313b-114">Cell name:</span></span>  <br/> |<span data-ttu-id="c313b-115">Char.Overline [ *i* ]、 *i* = < 1 > 2 です。</span><span class="sxs-lookup"><span data-stu-id="c313b-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="c313b-116">3.</span><span class="sxs-lookup"><span data-stu-id="c313b-116">3...</span></span>  <br/> |
   
<span data-ttu-id="c313b-117">プログラムから、インデックスによって [Overline] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c313b-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c313b-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c313b-118">Section index:</span></span>  <br/> |<span data-ttu-id="c313b-119">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="c313b-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="c313b-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c313b-120">Row index:</span></span>  <br/> |<span data-ttu-id="c313b-121">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="c313b-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c313b-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c313b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c313b-123">**visCharacterOverline**</span><span class="sxs-lookup"><span data-stu-id="c313b-123">**visCharacterOverline**</span></span> <br/> |
   

