---
title: '[スタイル エクスプローラー] ウィンドウについて'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: '[スタイル エクスプローラー] ウィンドウでは、特定のスタイルから継承される図形セル、または特定のセルがその値を継承するスタイルを、図形作成者が即座に決定できます。'
ms.openlocfilehash: 25af478b8ac4e35c7ae0b88bf69aad21d679da17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804733"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="eddff-103">スタイル エクスプローラー ウィンドウについて</span><span class="sxs-lookup"><span data-stu-id="eddff-103">About the Style Explorer Window</span></span>

<span data-ttu-id="eddff-104">[**スタイル エクスプローラー**] ウィンドウでは、特定のスタイルから継承される図形セル、または特定のセルがその値を継承するスタイルを、図形作成者が即座に決定できます。</span><span class="sxs-lookup"><span data-stu-id="eddff-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="eddff-p101">スタイルは、図形への適用が可能な書式属性の、名前付きコレクションです。Microsoft Visio では、1 つのスタイルにテキスト属性、線属性および塗りつぶし属性を定義して、図形内の一貫性を効率的に確保する手段として利用できます。また、いずれか 1 つの属性のクラス (テキスト、線、または塗りつぶし) または属性の組み合わせに対するスタイルを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="eddff-p101">Styles are named collections of formatting attributes that you can apply to a shape. In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes. Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="eddff-108">図形の書式をスタイルから適用すると、書式属性を個別に適用した図形とは異なり、一貫性が確保されるだけではなく、図形の作成、移動、拡大縮小、または回転時の動作が高速になります。</span><span class="sxs-lookup"><span data-stu-id="eddff-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="eddff-109">**スタイル エクスプ**ローラー] ウィンドウは、図形に対して行う変更の意味合いをより深く理解する必要がある情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="eddff-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eddff-110">[シェイプシート] ウィンドウでは、継承されたセル値は黒色で表示されるのに対し、ローカルのセル値は青色で表示されます。</span><span class="sxs-lookup"><span data-stu-id="eddff-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="eddff-111">[スタイル エクスプローラー] ウィンドウの使用</span><span class="sxs-lookup"><span data-stu-id="eddff-111">Using the Style Explorer window</span></span>

<span data-ttu-id="eddff-112">**シェイプ ツールのデザイン**] タブの [**表示**] で、[**スタイル エクスプ ローラー** ] ウィンドウの [シェイプ シート] ウィンドウをアクティブにしてを表示するには、 **[スタイル エクスプ ローラー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eddff-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="eddff-113">**[スタイル エクスプ ローラー**ウィンドウ ドッキングされて表示されます、[シェイプ シート] ウィンドウで、既定でですが、アンカー ウィンドウのドッキングできる、フロート、またはその他の利用可能なシェイプ シート ウィンドウ、 **[数式トレース**] ウィンドウなどと結合します。</span><span class="sxs-lookup"><span data-stu-id="eddff-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="eddff-114">**スタイル エクスプ**ローラー] ウィンドウには、現在の図面で定義されているすべてのスタイルのツリー ビューで表示が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eddff-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eddff-115">スタイルの情報を取得するには、[**スタイル エクスプローラー**] ウィンドウでスタイルを右クリックして、その [シェイプシート] を表示します。</span><span class="sxs-lookup"><span data-stu-id="eddff-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="eddff-116">[**スタイル エクスプローラー**] ウィンドウでは、次の情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="eddff-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="eddff-117">選択されたスタイルから値を継承するセル[**スタイル エクスプローラー**] ウィンドウでスタイルを選択すると、[シェイプシート] ウィンドウ内にあるセルのうちスタイルを継承するものはすべてハッチングなしで表示されるのに対し、スタイルを継承しないものはハッチングが薄く表示されます。</span><span class="sxs-lookup"><span data-stu-id="eddff-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="eddff-118">選択されたセルがその値を継承するスタイルシェイプシートのセルを選択すると、[シェイプシート] ウィンドウの下にあるタスク バーに、その値を継承するスタイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eddff-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

