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
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423868"
---
# <a name="about-error-values"></a><span data-ttu-id="bec32-103">エラー値について</span><span class="sxs-lookup"><span data-stu-id="bec32-103">About Error Values</span></span>

<span data-ttu-id="bec32-104">エラー値は、誤った数式を含むセルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="bec32-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="bec32-p101">数式がエラー値を含むセルを参照すると、その数式にもエラー値が表示されます。ISERR、ISERRNA、ISERROR、または ISERRVALUE 関数を使用してエラー値を検索できます。</span><span class="sxs-lookup"><span data-stu-id="bec32-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="bec32-107">**エラー値**</span><span class="sxs-lookup"><span data-stu-id="bec32-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="bec32-108">**セルでの表示**</span><span class="sxs-lookup"><span data-stu-id="bec32-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="bec32-109">**数式に含まれているエラー**</span><span class="sxs-lookup"><span data-stu-id="bec32-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="bec32-110">**例**</span><span class="sxs-lookup"><span data-stu-id="bec32-110">**Example**</span></span> <br/> |
| <span data-ttu-id="bec32-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="bec32-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="bec32-112">0 による除算</span><span class="sxs-lookup"><span data-stu-id="bec32-112">Division by 0</span></span>  <br/> |<span data-ttu-id="bec32-113">10/0</span><span class="sxs-lookup"><span data-stu-id="bec32-113">10/0</span></span>  <br/> |
| <span data-ttu-id="bec32-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="bec32-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="bec32-115">間違ったタイプの引数またはオペランド。</span><span class="sxs-lookup"><span data-stu-id="bec32-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="bec32-116">5 + "House"</span><span class="sxs-lookup"><span data-stu-id="bec32-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="bec32-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="bec32-117">#REF!</span></span>  <br/> | <span data-ttu-id="bec32-118">存在しないセルへの参照</span><span class="sxs-lookup"><span data-stu-id="bec32-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="bec32-119">存在しない別のセルを参照するセル</span><span class="sxs-lookup"><span data-stu-id="bec32-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="bec32-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="bec32-120">#NUM!</span></span>  <br/> | <span data-ttu-id="bec32-121">無効な数値</span><span class="sxs-lookup"><span data-stu-id="bec32-121">An invalid number</span></span>  <br/> | <span data-ttu-id="bec32-122">負の数値の平方根</span><span class="sxs-lookup"><span data-stu-id="bec32-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="bec32-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="bec32-123">#N/A!</span></span>  <br/> | <span data-ttu-id="bec32-124">使用できない値</span><span class="sxs-lookup"><span data-stu-id="bec32-124">Not an available value</span></span>  <br/> | <span data-ttu-id="bec32-125">NA 関数</span><span class="sxs-lookup"><span data-stu-id="bec32-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="bec32-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="bec32-126">#DIM!</span></span>  <br/> | <span data-ttu-id="bec32-127">次元の範囲を超える次元の値 (有効な指数は -128 \<= n \<= 127 の範囲の整数)</span><span class="sxs-lookup"><span data-stu-id="bec32-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="bec32-128">不適切な操作で使用される次元の値</span><span class="sxs-lookup"><span data-stu-id="bec32-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="bec32-129">1in^100 \* 1in^100 (結果は 1in^200 となり、次元の範囲を超える)</span><span class="sxs-lookup"><span data-stu-id="bec32-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="bec32-130">5.2cm^1.5 (指数が整数ではない)</span><span class="sxs-lookup"><span data-stu-id="bec32-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

