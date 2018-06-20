---
title: '[SortKey] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: '[図形データ] ウィンドウ内の項目が表示されている順序に影響を与える文字列と評価されます。'
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806551"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="83b40-103">[SortKey] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="83b40-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="83b40-104">[**図形データ**] ウィンドウ内の項目が表示されている順序に影響を与える文字列と評価されます。</span><span class="sxs-lookup"><span data-stu-id="83b40-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83b40-105">備考</span><span class="sxs-lookup"><span data-stu-id="83b40-105">Remarks</span></span>

<span data-ttu-id="83b40-106">[Sortkey] の値を比較するために使用する計算は、およびロケール固有の大文字小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="83b40-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="83b40-107">[Sortkey] の値が等しい場合は、図形データ行の順序が表示されます。</span><span class="sxs-lookup"><span data-stu-id="83b40-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="83b40-108">並べ替えキーが図形データは、並べ替えキーが含まれている図形データの後に一覧表示されません。</span><span class="sxs-lookup"><span data-stu-id="83b40-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="83b40-109">次の順序で、[**図形データ**] ウィンドウで図形データを表示するのには並べ替えキーを使用する場合の例: 品目番号、数量、価格です。</span><span class="sxs-lookup"><span data-stu-id="83b40-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="83b40-110">*行ラベル、* および *[sortkey]* は、図形データ行のセルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b40-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="83b40-111">この例では、図形データ行に名前が付いています。</span><span class="sxs-lookup"><span data-stu-id="83b40-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="83b40-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="83b40-112">**Row**</span></span>|<span data-ttu-id="83b40-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="83b40-113">**Label**</span></span>|<span data-ttu-id="83b40-114">**[Sortkey]**</span><span class="sxs-lookup"><span data-stu-id="83b40-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="83b40-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="83b40-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="83b40-116">項目番号</span><span class="sxs-lookup"><span data-stu-id="83b40-116">Item Number</span></span>  <br/> | <span data-ttu-id="83b40-117">1</span><span class="sxs-lookup"><span data-stu-id="83b40-117">1</span></span>  <br/> |
| <span data-ttu-id="83b40-118">付ける</span><span class="sxs-lookup"><span data-stu-id="83b40-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="83b40-119">価格</span><span class="sxs-lookup"><span data-stu-id="83b40-119">Price</span></span>  <br/> | <span data-ttu-id="83b40-120">3</span><span class="sxs-lookup"><span data-stu-id="83b40-120">3</span></span>  <br/> |
| <span data-ttu-id="83b40-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="83b40-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="83b40-122">数量</span><span class="sxs-lookup"><span data-stu-id="83b40-122">Quantity</span></span>  <br/> | <span data-ttu-id="83b40-123">2</span><span class="sxs-lookup"><span data-stu-id="83b40-123">2</span></span>  <br/> |
   
<span data-ttu-id="83b40-124">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [sortkey] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="83b40-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83b40-125">セル名:</span><span class="sxs-lookup"><span data-stu-id="83b40-125">Cell name:</span></span>  <br/> | <span data-ttu-id="83b40-126">プロペラです。 *名*です。[Sortkey] プロパティでは。 *名前*は、カスタム プロパティ行の名前</span><span class="sxs-lookup"><span data-stu-id="83b40-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="83b40-127">プログラムから、インデックスによって [sortkey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="83b40-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83b40-128">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="83b40-128">Section index:</span></span>  <br/> |<span data-ttu-id="83b40-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="83b40-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="83b40-130">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="83b40-130">Row index:</span></span>  <br/> |<span data-ttu-id="83b40-131">**visRowProp** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="83b40-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="83b40-132">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="83b40-132">Cell index:</span></span>  <br/> |<span data-ttu-id="83b40-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="83b40-133">**visCustPropsSortKey**</span></span> <br/> |
   

