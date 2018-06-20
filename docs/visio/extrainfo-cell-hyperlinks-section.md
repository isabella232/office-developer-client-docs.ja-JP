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
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="f7155-104">[ExtraInfo] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="f7155-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="f7155-105">イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。</span><span class="sxs-lookup"><span data-stu-id="f7155-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="f7155-106">ExtraInfo] セルで、"x = 41&amp;y = 7"イメージ マップの座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7155-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7155-107">備考</span><span class="sxs-lookup"><span data-stu-id="f7155-107">Remarks</span></span>

<span data-ttu-id="f7155-108">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="f7155-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="f7155-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ExtraInfo] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f7155-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7155-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="f7155-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f7155-111">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="f7155-111">Hyperlink.</span></span>  <span data-ttu-id="f7155-112">*名*です。ExtraInfo いるハイパーリンク。</span><span class="sxs-lookup"><span data-stu-id="f7155-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="f7155-113">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="f7155-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f7155-114">プログラムから、インデックスによって [ExtraInfo] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7155-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7155-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7155-115">Section index:</span></span>  <br/> |<span data-ttu-id="f7155-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="f7155-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="f7155-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7155-117">Row index:</span></span>  <br/> |<span data-ttu-id="f7155-118">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="f7155-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f7155-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7155-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f7155-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="f7155-120">**visHLinkExtraInfo**</span></span> <br/> |
   

