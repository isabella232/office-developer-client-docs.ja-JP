---
title: '[Value] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: 図形データの定義] ダイアログ ボックスに入力した図形データ項目の値が含まれています。
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806759"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="066ed-103">[Value] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="066ed-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="066ed-104">**図形データの定義**] ダイアログ ボックスに入力した図形データ項目の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="066ed-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="066ed-105">備考</span><span class="sxs-lookup"><span data-stu-id="066ed-105">Remarks</span></span>

<span data-ttu-id="066ed-106">このセルに数式を入力は、[**図形データの定義**] ダイアログ ボックスで入力した値によって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="066ed-106">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="066ed-107">GUARD 関数を使用して数式を保護する場合でも同様です。</span><span class="sxs-lookup"><span data-stu-id="066ed-107">This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="066ed-108">取得する [値] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="066ed-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="066ed-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="066ed-109">Cell name:</span></span>  <br/> | <span data-ttu-id="066ed-110">プロペラです。 *名*です。値、プロパティです。 *名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="066ed-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="066ed-111">プログラムから、インデックスによって [Value] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="066ed-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="066ed-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="066ed-112">Section index:</span></span>  <br/> |<span data-ttu-id="066ed-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="066ed-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="066ed-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="066ed-114">Row index:</span></span>  <br/> |<span data-ttu-id="066ed-115">**visRowProp** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="066ed-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="066ed-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="066ed-116">Cell index:</span></span>  <br/> |<span data-ttu-id="066ed-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="066ed-117">**visCustPropsValue**</span></span> <br/> |
   

