---
title: SETATREFEXPR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: ユーザーインターフェイス (UI) またはオートメーションのアクションによって設定された値を格納します。
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326006"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="6852f-103">SETATREFEXPR 関数</span><span class="sxs-lookup"><span data-stu-id="6852f-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="6852f-104">ユーザーインターフェイス (UI) またはオートメーションのアクションによって設定された値を格納します。</span><span class="sxs-lookup"><span data-stu-id="6852f-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6852f-105">構文</span><span class="sxs-lookup"><span data-stu-id="6852f-105">Syntax</span></span>

<span data-ttu-id="6852f-106">SETATREFEXPR ([\* \* *expr_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="6852f-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6852f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6852f-107">Parameters</span></span>

|<span data-ttu-id="6852f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6852f-108">**Name**</span></span>|<span data-ttu-id="6852f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6852f-109">**Required/Optional**</span></span>|<span data-ttu-id="6852f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6852f-110">**Data Type**</span></span>|<span data-ttu-id="6852f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6852f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6852f-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="6852f-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="6852f-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="6852f-113">Optional</span></span>  <br/> |<span data-ttu-id="6852f-114">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="6852f-114">**Varies**</span></span> <br/> |<span data-ttu-id="6852f-115">SETATREF 関数で参照先のセルに割り当てられる値または式によって置き換えられる式を指定します。</span><span class="sxs-lookup"><span data-stu-id="6852f-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="6852f-116">指定しない場合、初期値は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="6852f-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6852f-117">解説</span><span class="sxs-lookup"><span data-stu-id="6852f-117">Remarks</span></span>

<span data-ttu-id="6852f-118">SETATREFEXPR 式の値は、SETATREFEXPR 式を含むセルを参照する別のセルの SETATREF 関数から設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6852f-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="6852f-119">SETATREF 関数のパラメーターとして SETATREFEXPR 関数を使用することに制限はありません。</span><span class="sxs-lookup"><span data-stu-id="6852f-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6852f-120">例 1</span><span class="sxs-lookup"><span data-stu-id="6852f-120">Example 1</span></span>

<span data-ttu-id="6852f-121">次の例では、SETATREFEXPR 関数を使用して、図形の幅がそのテキストの幅と同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6852f-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="6852f-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="6852f-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6852f-123">例 2</span><span class="sxs-lookup"><span data-stu-id="6852f-123">Example 2</span></span>

<span data-ttu-id="6852f-p102">次の例では、SETATREFEXPR 関数を使用して、図形をカスタム グリッドにスナップする方法を示します。SETATREFEXPR 数式は  [PinX] および [PinY] セルに設定され、図形のピンは [User.GridX] および [User.GridY] で定義されたグリッドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="6852f-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="6852f-126">User.GridX =2 in</span><span class="sxs-lookup"><span data-stu-id="6852f-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="6852f-127">User.GridY =2 in</span><span class="sxs-lookup"><span data-stu-id="6852f-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="6852f-128">PinX = INT (SETATREFEXPR ()/User.GridX + .5)\*GridX</span><span class="sxs-lookup"><span data-stu-id="6852f-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="6852f-129">PinY = INT (SETATREFEXPR ()/User.GridY + .5)\*ユーザー. GridY</span><span class="sxs-lookup"><span data-stu-id="6852f-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6852f-130">例 3</span><span class="sxs-lookup"><span data-stu-id="6852f-130">Example 3</span></span>

<span data-ttu-id="6852f-131">SETATREFEXPR 関数を SETATREF 関数と共に使用する例については、[SETATREF](setatref-function.md) 関数を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6852f-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

