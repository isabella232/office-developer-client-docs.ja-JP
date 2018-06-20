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
description: '[図形データ] ウィンドウの図形データ項目が表示されているかどうかを指定します。'
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805592"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="4b460-103">[Invisible] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="4b460-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="4b460-104">[**図形データ**] ウィンドウの図形データ項目が表示されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4b460-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="4b460-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4b460-105">**Value**</span></span>|<span data-ttu-id="4b460-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="4b460-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4b460-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4b460-107">TRUE</span></span>  <br/> | <span data-ttu-id="4b460-108">図形データ項目を表示しません。</span><span class="sxs-lookup"><span data-stu-id="4b460-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="4b460-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4b460-109">FALSE</span></span>  <br/> | <span data-ttu-id="4b460-110">図形データ項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="4b460-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b460-111">注釈</span><span class="sxs-lookup"><span data-stu-id="4b460-111">Remarks</span></span>

<span data-ttu-id="4b460-112">このセルの値の対応する**図形データの定義**] ダイアログ ボックスで [**隠し文字**] チェック ボックス (図形を右クリックし、**データ**をポイントし、[**図形データの定義**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="4b460-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="4b460-113">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって非表示のセルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4b460-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b460-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="4b460-114">Cell name:</span></span>  <br/> | <span data-ttu-id="4b460-115">プロペラです。 *名*です。非表示の場所のプロパティです。 *名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="4b460-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="4b460-116">プログラムから、インデックスによって [Invisible] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4b460-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b460-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4b460-117">Section index:</span></span>  <br/> |<span data-ttu-id="4b460-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="4b460-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="4b460-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4b460-119">Row index:</span></span>  <br/> |<span data-ttu-id="4b460-120">**visRowProp** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="4b460-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4b460-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4b460-121">Cell index:</span></span>  <br/> |<span data-ttu-id="4b460-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="4b460-122">**visCustPropsInvis**</span></span> <br/> |
   

