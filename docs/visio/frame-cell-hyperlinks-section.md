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
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805453"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="e1f14-104">[Frame] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="e1f14-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="e1f14-p102">コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="e1f14-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1f14-107">備考</span><span class="sxs-lookup"><span data-stu-id="e1f14-107">Remarks</span></span>

<span data-ttu-id="e1f14-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Frame] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e1f14-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1f14-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="e1f14-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e1f14-110">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="e1f14-110">Hyperlink.</span></span>  <span data-ttu-id="e1f14-111">*名*です。フレームの場所のハイパーリンクです。</span><span class="sxs-lookup"><span data-stu-id="e1f14-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="e1f14-112">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="e1f14-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="e1f14-113">プログラムから、インデックスによって [Frame] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e1f14-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1f14-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e1f14-114">Section index:</span></span>  <br/> |<span data-ttu-id="e1f14-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="e1f14-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="e1f14-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e1f14-116">Row index:</span></span>  <br/> |<span data-ttu-id="e1f14-117">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="e1f14-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e1f14-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e1f14-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e1f14-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="e1f14-119">**visHLinkFrame**</span></span> <br/> |
   

