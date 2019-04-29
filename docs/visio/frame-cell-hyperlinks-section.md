---
title: '[Frame] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432857"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="a72c4-104">[Frame] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="a72c4-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="a72c4-p102">コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="a72c4-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a72c4-107">注釈</span><span class="sxs-lookup"><span data-stu-id="a72c4-107">Remarks</span></span>

<span data-ttu-id="a72c4-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Frame] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a72c4-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a72c4-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="a72c4-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a72c4-110">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="a72c4-110">Hyperlink.</span></span>  <span data-ttu-id="a72c4-111">*名前*です。ハイパーリンクのフレーム。</span><span class="sxs-lookup"><span data-stu-id="a72c4-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="a72c4-112">*name*には、行の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a72c4-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="a72c4-113">プログラムから、インデックスによって [Frame] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a72c4-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a72c4-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a72c4-114">Section index:</span></span>  <br/> |<span data-ttu-id="a72c4-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="a72c4-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="a72c4-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a72c4-116">Row index:</span></span>  <br/> |<span data-ttu-id="a72c4-117">**visRow1stHyperlink** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="a72c4-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a72c4-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a72c4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a72c4-119">**vishlinkframe**</span><span class="sxs-lookup"><span data-stu-id="a72c4-119">**visHLinkFrame**</span></span> <br/> |
   

