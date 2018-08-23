---
title: '[ExtraInfo] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 ExtraInfo] セルで、x = 41&amp;y 7specifies のイメージ マップの座標を = します。
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805355"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="5a435-104">[ExtraInfo] セル ([ハイパーリンク] セクション)</span><span class="sxs-lookup"><span data-stu-id="5a435-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="5a435-105">イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。</span><span class="sxs-lookup"><span data-stu-id="5a435-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="5a435-106">ExtraInfo] セルで、"x = 41&amp;y = 7"イメージ マップの座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a435-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a435-107">備考</span><span class="sxs-lookup"><span data-stu-id="5a435-107">Remarks</span></span>

<span data-ttu-id="5a435-108">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="5a435-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="5a435-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ExtraInfo] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5a435-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a435-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="5a435-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5a435-111">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="5a435-111">Hyperlink.</span></span>  <span data-ttu-id="5a435-112">*名*です。ExtraInfo いるハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="5a435-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="5a435-113">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="5a435-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="5a435-114">プログラムから、インデックスによって [ExtraInfo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a435-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a435-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5a435-115">Section index:</span></span>  <br/> |<span data-ttu-id="5a435-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="5a435-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="5a435-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5a435-117">Row index:</span></span>  <br/> |<span data-ttu-id="5a435-118">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="5a435-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5a435-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5a435-119">Cell index:</span></span>  <br/> |<span data-ttu-id="5a435-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="5a435-120">**visHLinkExtraInfo**</span></span> <br/> |
   

