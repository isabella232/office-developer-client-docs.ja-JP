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
description: イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 たとえば、[ExtraInfo] セルの x = 41&amp;y = 7specifies、イメージマップの座標を指定します。
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409574"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="6aac1-104">[ExtraInfo] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="6aac1-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="6aac1-105">イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。</span><span class="sxs-lookup"><span data-stu-id="6aac1-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="6aac1-106">たとえば、[ExtraInfo] セルの "x = 41&amp;y = 7" では、イメージマップの座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="6aac1-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6aac1-107">注釈</span><span class="sxs-lookup"><span data-stu-id="6aac1-107">Remarks</span></span>

<span data-ttu-id="6aac1-108">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="6aac1-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="6aac1-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ExtraInfo] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6aac1-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6aac1-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="6aac1-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6aac1-111">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="6aac1-111">Hyperlink.</span></span>  <span data-ttu-id="6aac1-112">*名前*です。引数 ExtraInfo のハイパーリンクを指定します。</span><span class="sxs-lookup"><span data-stu-id="6aac1-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="6aac1-113">*name*には、行の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6aac1-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6aac1-114">プログラムから、インデックスによって [ExtraInfo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6aac1-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6aac1-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6aac1-115">Section index:</span></span>  <br/> |<span data-ttu-id="6aac1-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="6aac1-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="6aac1-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6aac1-117">Row index:</span></span>  <br/> |<span data-ttu-id="6aac1-118">**visRow1stHyperlink** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="6aac1-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6aac1-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6aac1-119">Cell index:</span></span>  <br/> |<span data-ttu-id="6aac1-120">**vishlinkextrainfo**</span><span class="sxs-lookup"><span data-stu-id="6aac1-120">**visHLinkExtraInfo**</span></span> <br/> |
   

