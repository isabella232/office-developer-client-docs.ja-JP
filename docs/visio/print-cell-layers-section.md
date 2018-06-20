---
title: '[Print] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: レイヤーに属している図形が印刷可能かどうかを指定します。
ms.openlocfilehash: cd5b2830ba8bd20cb435cdc2bca4bd55fd5a5438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806106"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="0bc1e-103">[Print] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="0bc1e-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="0bc1e-104">レイヤーに属している図形が印刷可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0bc1e-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="0bc1e-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0bc1e-105">**Value**</span></span>|<span data-ttu-id="0bc1e-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="0bc1e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0bc1e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0bc1e-107">TRUE</span></span>  <br/> |<span data-ttu-id="0bc1e-108">図形を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="0bc1e-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="0bc1e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc1e-109">FALSE</span></span>  <br/> |<span data-ttu-id="0bc1e-110">図形を印刷できません。</span><span class="sxs-lookup"><span data-stu-id="0bc1e-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bc1e-111">注釈</span><span class="sxs-lookup"><span data-stu-id="0bc1e-111">Remarks</span></span>

<span data-ttu-id="0bc1e-112">**[レイヤー プロパティ**] ダイアログ ボックスで **[印刷**] オプションを使用してこの値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="0bc1e-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="0bc1e-113">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Print] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="0bc1e-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bc1e-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="0bc1e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="0bc1e-115">Layers.Print [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="0bc1e-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0bc1e-116">プログラムから、インデックスによって [Print] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0bc1e-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bc1e-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0bc1e-117">Section index:</span></span>  <br/> |<span data-ttu-id="0bc1e-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="0bc1e-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="0bc1e-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0bc1e-119">Row index:</span></span>  <br/> |<span data-ttu-id="0bc1e-120">**visRowLayer** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="0bc1e-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0bc1e-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0bc1e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="0bc1e-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="0bc1e-122">**visDocPreviewScope**</span></span> <br/> |
   

