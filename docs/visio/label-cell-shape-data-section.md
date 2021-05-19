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
description: '[図形データ] ウィンドウに表示されるラベルを指定します。ラベルには、英数字とアンダースコア (_) 文字を使用できます。'
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420179"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="9b34d-104">[Label] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="9b34d-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="9b34d-p102">[**図形データ**] ウィンドウに表示されるラベルを指定します。ラベルには、英数字とアンダースコア (_) 文字を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b34d-p102">Specifies the label that appears to users in the **Shape Data** window. A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9b34d-107">注釈</span><span class="sxs-lookup"><span data-stu-id="9b34d-107">Remarks</span></span>

<span data-ttu-id="9b34d-108">このセルではラベルの文字列が自動的に引用符で囲まれますが、[**図形データ**] ウィンドウでは引用符は表示されません。</span><span class="sxs-lookup"><span data-stu-id="9b34d-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="9b34d-109">ラベル テキストがない場合、[**図形データ**] ウィンドウには行の名前 (Prop.Row) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b34d-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="9b34d-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Label] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b34d-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b34d-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="9b34d-111">Cell name:</span></span>  <br/> |<span data-ttu-id="9b34d-112">Prop. *Name*  .Prop のラベル。  *名前*  は行名です</span><span class="sxs-lookup"><span data-stu-id="9b34d-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="9b34d-113">プログラムから、インデックスによって [Label] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b34d-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b34d-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b34d-114">Section index:</span></span>  <br/> |<span data-ttu-id="9b34d-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="9b34d-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="9b34d-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b34d-116">Row index:</span></span>  <br/> |<span data-ttu-id="9b34d-117">**visRowProp**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9b34d-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9b34d-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9b34d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9b34d-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="9b34d-119">**visCustPropsLabel**</span></span> <br/> |
   

