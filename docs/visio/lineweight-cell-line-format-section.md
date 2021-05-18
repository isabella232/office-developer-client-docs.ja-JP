---
title: '[LineWeight] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: 図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412248"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="2ccf9-104">[LineWeight] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="2ccf9-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="2ccf9-p102">図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ccf9-p102">Determines the line weight of a shape. Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ccf9-107">注釈</span><span class="sxs-lookup"><span data-stu-id="2ccf9-107">Remarks</span></span>

<span data-ttu-id="2ccf9-108">LineWeight の値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを表示するには、[**ホーム**] タブの [**図形**] で、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="2ccf9-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="2ccf9-109">単位を入力しない場合は **、[Visio オプション**] ダイアログ ボックスで指定したテキストの測定単位が使用されます ([ファイル]タブをクリックし、[オプション] をクリック **します**)。</span><span class="sxs-lookup"><span data-stu-id="2ccf9-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="2ccf9-110">線の太さは、図面の縮尺による影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="2ccf9-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="2ccf9-111">図面の縮尺を変更しても、線の太さは変わりません。</span><span class="sxs-lookup"><span data-stu-id="2ccf9-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="2ccf9-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineWeight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2ccf9-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ccf9-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="2ccf9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2ccf9-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="2ccf9-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="2ccf9-115">プログラムから、インデックスによって [LineWeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ccf9-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ccf9-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ccf9-116">Section index:</span></span>  <br/> |<span data-ttu-id="2ccf9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2ccf9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2ccf9-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ccf9-118">Row index:</span></span>  <br/> |<span data-ttu-id="2ccf9-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="2ccf9-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="2ccf9-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2ccf9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2ccf9-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="2ccf9-121">**visLineWeight**</span></span> <br/> |
   

