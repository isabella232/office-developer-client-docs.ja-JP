---
title: '[Invisible] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: '[図形データ] ウィンドウに、図形データ項目を表示するかどうかを指定します。'
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405318"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="9b1ce-103">[Invisible] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="9b1ce-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="9b1ce-104">[**図形データ**] ウィンドウに、図形データ項目を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9b1ce-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="9b1ce-105">**値**</span><span class="sxs-lookup"><span data-stu-id="9b1ce-105">**Value**</span></span>|<span data-ttu-id="9b1ce-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="9b1ce-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9b1ce-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9b1ce-107">TRUE</span></span>  <br/> | <span data-ttu-id="9b1ce-108">図形データ項目を表示しません。</span><span class="sxs-lookup"><span data-stu-id="9b1ce-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="9b1ce-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9b1ce-109">FALSE</span></span>  <br/> | <span data-ttu-id="9b1ce-110">図形データ項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="9b1ce-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b1ce-111">注釈</span><span class="sxs-lookup"><span data-stu-id="9b1ce-111">Remarks</span></span>

<span data-ttu-id="9b1ce-112">このセルの値は、[**図形データの定義**] ダイアログ ボックスの [**表示しない**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、図形を右クリックし、[**データ**] をポイントして、[**図形データの定義**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="9b1ce-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="9b1ce-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b1ce-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b1ce-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="9b1ce-114">Cell name:</span></span>  <br/> | <span data-ttu-id="9b1ce-115">提案. *名前*です。Prop の場合は非表示です。 *name*には、行の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b1ce-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="9b1ce-116">プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b1ce-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b1ce-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b1ce-117">Section index:</span></span>  <br/> |<span data-ttu-id="9b1ce-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="9b1ce-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="9b1ce-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b1ce-119">Row index:</span></span>  <br/> |<span data-ttu-id="9b1ce-120">**visRowProp** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="9b1ce-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9b1ce-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b1ce-121">Cell index:</span></span>  <br/> |<span data-ttu-id="9b1ce-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="9b1ce-122">**visCustPropsInvis**</span></span> <br/> |
   

