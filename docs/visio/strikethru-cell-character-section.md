---
title: '[Strikethru] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: テキストを取り消し線として書式設定するかどうかを指定します。
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806585"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="af522-103">[Strikethru] セル ([文字] セクション)</span><span class="sxs-lookup"><span data-stu-id="af522-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="af522-104">テキストを取り消し線として書式設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="af522-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="af522-105">**値**</span><span class="sxs-lookup"><span data-stu-id="af522-105">**Value**</span></span>|<span data-ttu-id="af522-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="af522-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af522-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="af522-107">TRUE</span></span>  <br/> |<span data-ttu-id="af522-108">テキストを取り消し線として書式設定します。</span><span class="sxs-lookup"><span data-stu-id="af522-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="af522-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="af522-109">FALSE</span></span>  <br/> |<span data-ttu-id="af522-110">テキストを取り消し線として書式設定しません。</span><span class="sxs-lookup"><span data-stu-id="af522-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af522-111">注釈</span><span class="sxs-lookup"><span data-stu-id="af522-111">Remarks</span></span>

<span data-ttu-id="af522-112">このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="af522-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="af522-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Strikethru] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="af522-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af522-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="af522-114">Cell name:</span></span>  <br/> |<span data-ttu-id="af522-115">Char.Strikethru [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="af522-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="af522-116">プログラムから、インデックスによって [Strikethru] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="af522-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af522-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="af522-117">Section index:</span></span>  <br/> |<span data-ttu-id="af522-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="af522-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="af522-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="af522-119">Row index:</span></span>  <br/> |<span data-ttu-id="af522-120">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="af522-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="af522-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="af522-121">Cell index:</span></span>  <br/> |<span data-ttu-id="af522-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="af522-122">**visCharacterStrikethru**</span></span> <br/> |
   

