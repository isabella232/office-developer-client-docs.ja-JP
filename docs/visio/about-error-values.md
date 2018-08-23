---
title: エラー値について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: エラー値は、誤った数式を含むセルに表示されます。
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804729"
---
# <a name="about-error-values"></a><span data-ttu-id="7ba17-103">エラー値について</span><span class="sxs-lookup"><span data-stu-id="7ba17-103">About Error Values</span></span>

<span data-ttu-id="7ba17-104">エラー値は、誤った数式を含むセルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ba17-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="7ba17-p101">数式がエラー値を含むセルを参照すると、その数式にもエラー値が表示されます。ISERR、ISERRNA、ISERROR、または ISERRVALUE 関数を使用してエラー値を検索できます。</span><span class="sxs-lookup"><span data-stu-id="7ba17-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="7ba17-107">**エラー値**</span><span class="sxs-lookup"><span data-stu-id="7ba17-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="7ba17-108">**セルに表示されるエラー値 **</span><span class="sxs-lookup"><span data-stu-id="7ba17-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="7ba17-109">**数式に含まれているエラーの内容**</span><span class="sxs-lookup"><span data-stu-id="7ba17-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="7ba17-110">**例**</span><span class="sxs-lookup"><span data-stu-id="7ba17-110">**Example**</span></span> <br/> |
| <span data-ttu-id="7ba17-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="7ba17-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="7ba17-112">
                0 による除算
</span><span class="sxs-lookup"><span data-stu-id="7ba17-112">Division by 0</span></span>  <br/> |<span data-ttu-id="7ba17-113">10/0</span><span class="sxs-lookup"><span data-stu-id="7ba17-113">10/0</span></span>  <br/> |
| <span data-ttu-id="7ba17-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="7ba17-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="7ba17-115">
                
                
                無効な種類の引数またはオペランド
</span><span class="sxs-lookup"><span data-stu-id="7ba17-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="7ba17-116">
                
                
                5 + "House"
</span><span class="sxs-lookup"><span data-stu-id="7ba17-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="7ba17-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="7ba17-117">#REF!</span></span>  <br/> | <span data-ttu-id="7ba17-118">
                
                
                存在しないセルへの参照
</span><span class="sxs-lookup"><span data-stu-id="7ba17-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="7ba17-119">
                
                
                存在しない別のセルを参照するようにセルを指定した場合
</span><span class="sxs-lookup"><span data-stu-id="7ba17-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="7ba17-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="7ba17-120">#NUM!</span></span>  <br/> | <span data-ttu-id="7ba17-121">
                
                
                無効な数値
</span><span class="sxs-lookup"><span data-stu-id="7ba17-121">An invalid number</span></span>  <br/> | <span data-ttu-id="7ba17-122">
                
                
                負の数値の平方根
</span><span class="sxs-lookup"><span data-stu-id="7ba17-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="7ba17-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="7ba17-123">#N/A!</span></span>  <br/> | <span data-ttu-id="7ba17-124">使用可能な値ではありません。</span><span class="sxs-lookup"><span data-stu-id="7ba17-124">Not an available value</span></span>  <br/> | <span data-ttu-id="7ba17-125">
                
                
                NA( ) 関数
</span><span class="sxs-lookup"><span data-stu-id="7ba17-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="7ba17-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="7ba17-126">#DIM!</span></span>  <br/> | <span data-ttu-id="7ba17-127">寸法の範囲を超える寸法値 (有効な指数は、整数-128 \<n の = \<= 127)</span><span class="sxs-lookup"><span data-stu-id="7ba17-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="7ba17-128">不適切な演算で使用された寸法値
</span><span class="sxs-lookup"><span data-stu-id="7ba17-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="7ba17-129">1 in ^100\*に 1 ^100 (1 の結果は、^200 で、ディメンションの範囲を超えている)</span><span class="sxs-lookup"><span data-stu-id="7ba17-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="7ba17-130">5.2cm^1.5 (指数が整数ではない)
</span><span class="sxs-lookup"><span data-stu-id="7ba17-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

