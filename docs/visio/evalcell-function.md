---
title: EVALCELL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: (オプション) 引数としてユーザー定義関数に渡す 1 つ以上の名前/値ペアと同様に、カスタム関数を含むセルへの参照を受け取ります。 指定した引数と値を指定するユーザー定義関数の計算結果を返します。
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805319"
---
# <a name="evalcell-function"></a><span data-ttu-id="42883-104">EVALCELL 関数</span><span class="sxs-lookup"><span data-stu-id="42883-104">EVALCELL Function</span></span>

<span data-ttu-id="42883-105">(オプション) 引数としてユーザー定義関数に渡す 1 つ以上の名前/値ペアと同様に、カスタム関数を含むセルへの参照を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="42883-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="42883-106">指定した引数と値を指定するユーザー定義関数の計算結果を返します。</span><span class="sxs-lookup"><span data-stu-id="42883-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="42883-107">構文</span><span class="sxs-lookup"><span data-stu-id="42883-107">Syntax</span></span>

<span data-ttu-id="42883-108">EVALCELL (* * *cellRef* * *、[* * *arg1Name、arg1* * *]、[* * *arg2Name、arg2* * *],...)</span><span class="sxs-lookup"><span data-stu-id="42883-108">EVALCELL(** *cellRef* **,[ ** *arg1Name,arg1* ** ],[ ** *arg2Name,arg2* ** ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="42883-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="42883-109">Parameters</span></span>

|<span data-ttu-id="42883-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="42883-110">**Name**</span></span>|<span data-ttu-id="42883-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="42883-111">**Required/Optional**</span></span>|<span data-ttu-id="42883-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="42883-112">**Data Type**</span></span>|<span data-ttu-id="42883-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="42883-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="42883-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="42883-114">_cellRef_</span></span> <br/> |<span data-ttu-id="42883-115">必須</span><span class="sxs-lookup"><span data-stu-id="42883-115">Required</span></span>  <br/> |<span data-ttu-id="42883-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="42883-116">**String**</span></span> <br/> |<span data-ttu-id="42883-117">カスタム関数を含むセルへの参照。</span><span class="sxs-lookup"><span data-stu-id="42883-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="42883-118">シート間の参照は許可されています。</span><span class="sxs-lookup"><span data-stu-id="42883-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="42883-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="42883-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="42883-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="42883-120">Optional</span></span>  <br/> |<span data-ttu-id="42883-121">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="42883-121">**String**</span></span> <br/> |<span data-ttu-id="42883-p104">ユーザー設定関数に渡す 1 番目の引数の名前です。スペースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="42883-p104">The name of the first argument to be passed to the custom function. Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="42883-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="42883-124">_arg1_</span></span> <br/> |<span data-ttu-id="42883-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="42883-125">Optional</span></span>  <br/> |<span data-ttu-id="42883-126">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="42883-126">**Varies**</span></span> <br/> |<span data-ttu-id="42883-127">_Arg1_パラメーターの値です。</span><span class="sxs-lookup"><span data-stu-id="42883-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="42883-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="42883-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="42883-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="42883-129">Optional</span></span>  <br/> |<span data-ttu-id="42883-130">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="42883-130">**String**</span></span> <br/> |<span data-ttu-id="42883-131">ユーザー定義関数に渡される 2 番目の引数の名前。</span><span class="sxs-lookup"><span data-stu-id="42883-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="42883-132">スペースを使用します。</span><span class="sxs-lookup"><span data-stu-id="42883-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="42883-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="42883-133">_arg2_</span></span> <br/> |<span data-ttu-id="42883-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="42883-134">Optional</span></span>  <br/> |<span data-ttu-id="42883-135">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="42883-135">**Varies**</span></span> <br/> |<span data-ttu-id="42883-136">_Arg2_パラメーターの値です。</span><span class="sxs-lookup"><span data-stu-id="42883-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="42883-137">�߂�l</span><span class="sxs-lookup"><span data-stu-id="42883-137">Return value</span></span>

<span data-ttu-id="42883-138">数値</span><span class="sxs-lookup"><span data-stu-id="42883-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42883-139">注釈</span><span class="sxs-lookup"><span data-stu-id="42883-139">Remarks</span></span>

<span data-ttu-id="42883-140">呼び出し元のセルは、ユーザー設定関数が使用する引数をすべて指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="42883-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="42883-141">例</span><span class="sxs-lookup"><span data-stu-id="42883-141">Example</span></span>

<span data-ttu-id="42883-142">次の例は、3 つの値の集合から中央値を検索するために、ARG 関数と共に EVALCELL 関数を使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="42883-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="42883-143">式セルに、ユーザー設定関数を定義する次のコードを配置します。</span><span class="sxs-lookup"><span data-stu-id="42883-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="42883-144">呼び出しセルに、ユーザー設定関数を呼び出す次のコードを配置します。</span><span class="sxs-lookup"><span data-stu-id="42883-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


