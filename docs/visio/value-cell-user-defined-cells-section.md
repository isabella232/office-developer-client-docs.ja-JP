---
title: '[Value] セル ([User-Defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: 対応するユーザー定義のセルの値を指定します。
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355896"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="cad8a-103">[Value] セル ([User-Defined Cells] セクション)</span><span class="sxs-lookup"><span data-stu-id="cad8a-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="cad8a-104">対応するユーザー定義のセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cad8a-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cad8a-105">解説</span><span class="sxs-lookup"><span data-stu-id="cad8a-105">Remarks</span></span>

<span data-ttu-id="cad8a-106">別のセルでこの値を参照するには、行ラベル [User.Row] に入力したユーザー定義の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="cad8a-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="cad8a-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Value] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cad8a-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cad8a-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="cad8a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="cad8a-109">マニュアル.</span><span class="sxs-lookup"><span data-stu-id="cad8a-109">User.</span></span>  <span data-ttu-id="cad8a-110">*名前*です。Value (ユーザーの場合)。</span><span class="sxs-lookup"><span data-stu-id="cad8a-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="cad8a-111">*name*には、行の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="cad8a-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="cad8a-112">プログラムから、インデックスによって [Value] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cad8a-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cad8a-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cad8a-113">Section index:</span></span>  <br/> |<span data-ttu-id="cad8a-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="cad8a-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="cad8a-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cad8a-115">Row index:</span></span>  <br/> |<span data-ttu-id="cad8a-116">**visRowUser** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="cad8a-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cad8a-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cad8a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="cad8a-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="cad8a-118">**visUserValue**</span></span> <br/> |
   

