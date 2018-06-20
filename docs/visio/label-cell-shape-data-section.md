---
title: '[Label] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: '[図形データ] ウィンドウに表示されるラベルを指定します。 ラベルは、英数字、アンダー スコア (_) 文字で構成されます。'
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805634"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="73567-104">[Label] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="73567-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="73567-105">[**図形データ**] ウィンドウに表示されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="73567-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="73567-106">ラベルは、英数字、アンダー スコア (_) 文字で構成されます。</span><span class="sxs-lookup"><span data-stu-id="73567-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="73567-107">備考</span><span class="sxs-lookup"><span data-stu-id="73567-107">Remarks</span></span>

<span data-ttu-id="73567-108">アプリケーションは自動的に引用符で囲まれたセルのラベルの文字列を囲むが、[**図形データ**] ウィンドウでは引用符は表示されません。</span><span class="sxs-lookup"><span data-stu-id="73567-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="73567-109">ラベルのテキストが見つからない場合、[**図形データ**] ウィンドウで、行の名前 (Prop.Row) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="73567-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="73567-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Label] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="73567-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73567-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="73567-111">Cell name:</span></span>  <br/> |<span data-ttu-id="73567-112">プロペラです。*名*です。ラベル位置プロパティです。 *名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="73567-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="73567-113">プログラムから、インデックスによって [Label] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="73567-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73567-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="73567-114">Section index:</span></span>  <br/> |<span data-ttu-id="73567-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="73567-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="73567-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="73567-116">Row index:</span></span>  <br/> |<span data-ttu-id="73567-117">**visRowProp** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="73567-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="73567-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="73567-118">Cell index:</span></span>  <br/> |<span data-ttu-id="73567-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="73567-119">**visCustPropsLabel**</span></span> <br/> |
   

