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
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356183"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="95eda-103">[Print] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="95eda-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="95eda-104">レイヤーに属している図形が印刷可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="95eda-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="95eda-105">**値**</span><span class="sxs-lookup"><span data-stu-id="95eda-105">**Value**</span></span>|<span data-ttu-id="95eda-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="95eda-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95eda-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="95eda-107">TRUE</span></span>  <br/> |<span data-ttu-id="95eda-108">図形を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="95eda-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="95eda-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="95eda-109">FALSE</span></span>  <br/> |<span data-ttu-id="95eda-110">図形を印刷できません。</span><span class="sxs-lookup"><span data-stu-id="95eda-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95eda-111">解説</span><span class="sxs-lookup"><span data-stu-id="95eda-111">Remarks</span></span>

<span data-ttu-id="95eda-112">この値は、[**レイヤー プロパティ**] ダイアログ ボックスの [**印刷**] オプションを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="95eda-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="95eda-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Print] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95eda-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95eda-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="95eda-114">Cell name:</span></span>  <br/> |<span data-ttu-id="95eda-115"><1>、2、3のよう\*\* に、[ *i* ] を印刷します。</span><span class="sxs-lookup"><span data-stu-id="95eda-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95eda-116">プログラムから、インデックスによって [Print] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="95eda-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95eda-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="95eda-117">Section index:</span></span>  <br/> |<span data-ttu-id="95eda-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="95eda-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="95eda-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="95eda-119">Row index:</span></span>  <br/> |<span data-ttu-id="95eda-120">**visRowLayer** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="95eda-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="95eda-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="95eda-121">Cell index:</span></span>  <br/> |<span data-ttu-id="95eda-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="95eda-122">**visDocPreviewScope**</span></span> <br/> |
   

