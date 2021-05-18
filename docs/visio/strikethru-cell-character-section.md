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
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412430"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="c3657-103">[Strikethru] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="c3657-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="c3657-104">テキストを取り消し線として書式設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c3657-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="c3657-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c3657-105">**Value**</span></span>|<span data-ttu-id="c3657-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c3657-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c3657-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c3657-107">TRUE</span></span>  <br/> |<span data-ttu-id="c3657-108">テキストを取り消し線として書式設定します。</span><span class="sxs-lookup"><span data-stu-id="c3657-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="c3657-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c3657-109">FALSE</span></span>  <br/> |<span data-ttu-id="c3657-110">テキストを取り消し線として書式設定しません。</span><span class="sxs-lookup"><span data-stu-id="c3657-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3657-111">注釈</span><span class="sxs-lookup"><span data-stu-id="c3657-111">Remarks</span></span>

<span data-ttu-id="c3657-112">このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="c3657-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="c3657-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Strikethru] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c3657-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3657-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="c3657-114">Cell name:</span></span>  <br/> |<span data-ttu-id="c3657-115">Char.Strikethru[ i ]*ここで\*\*、i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="c3657-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c3657-116">プログラムから、インデックスによって [Strikethru] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3657-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3657-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c3657-117">Section index:</span></span>  <br/> |<span data-ttu-id="c3657-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="c3657-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="c3657-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c3657-119">Row index:</span></span>  <br/> |<span data-ttu-id="c3657-120">**visRowCharacter**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c3657-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c3657-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c3657-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c3657-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="c3657-122">**visCharacterStrikethru**</span></span> <br/> |
   

