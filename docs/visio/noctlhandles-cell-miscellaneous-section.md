---
title: '[NoCtlHandles] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: 選択した図形のコントロール ハンドルの表示/非表示を切り替えます。
ms.openlocfilehash: cbe4d6a8b6fdd4b66acf064884d20999ff7e3b4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319804"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a><span data-ttu-id="dd687-103">[NoCtlHandles] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="dd687-103">NoCtlHandles Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="dd687-104">選択した図形のコントロール ハンドルの表示/非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="dd687-104">Switches the display of control handles on and off for the selected shape.</span></span>
  
|<span data-ttu-id="dd687-105">**値**</span><span class="sxs-lookup"><span data-stu-id="dd687-105">**Value**</span></span>|<span data-ttu-id="dd687-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="dd687-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dd687-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd687-107">TRUE</span></span>  <br/> | <span data-ttu-id="dd687-108">図形を選択するときにコントロール ハンドルが表示されません。</span><span class="sxs-lookup"><span data-stu-id="dd687-108">Control handles are not displayed when a shape is selected.</span></span>  <br/> |
| <span data-ttu-id="dd687-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd687-109">FALSE</span></span>  <br/> | <span data-ttu-id="dd687-110">図形を選択するときにコントロール ハンドルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd687-110">Control handles are displayed when a shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd687-111">解説</span><span class="sxs-lookup"><span data-stu-id="dd687-111">Remarks</span></span>

<span data-ttu-id="dd687-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoCtlHandles] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="dd687-112">To get a reference to the NoCtlHandles cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd687-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="dd687-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dd687-114">[noctlhandles]</span><span class="sxs-lookup"><span data-stu-id="dd687-114">NoCtlHandles</span></span>  <br/> |
   
<span data-ttu-id="dd687-115">プログラムから、インデックスによる [NoCtlHandles] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dd687-115">To get a reference to the NoCtlHandles cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd687-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dd687-116">Section index:</span></span>  <br/> |<span data-ttu-id="dd687-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd687-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dd687-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dd687-118">Row index:</span></span>  <br/> |<span data-ttu-id="dd687-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="dd687-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="dd687-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dd687-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dd687-121">**visNoCtlHandles**</span><span class="sxs-lookup"><span data-stu-id="dd687-121">**visNoCtlHandles**</span></span> <br/> |
   

