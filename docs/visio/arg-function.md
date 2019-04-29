---
title: ARG 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: 呼び出し元のセルが引数の値を渡さない場合、ユーザー設定関数に渡すことができる引数と、ユーザー設定関数によって返される既定値を指定します。 呼び出し元のセルと一致する argname パラメーターで指定された値を返します。
ms.openlocfilehash: f85c3dc4a49878b034674330f272a63e79c17d49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422727"
---
# <a name="arg-function"></a><span data-ttu-id="5422b-104">ARG 関数</span><span class="sxs-lookup"><span data-stu-id="5422b-104">ARG Function</span></span>

<span data-ttu-id="5422b-105">呼び出し元のセルが引数の値を渡さない場合、ユーザー設定関数に渡すことができる引数と、ユーザー設定関数によって返される既定値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5422b-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="5422b-106">呼び出し元のセルと一致する argname パラメーターで指定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="5422b-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5422b-107">構文</span><span class="sxs-lookup"><span data-stu-id="5422b-107">Syntax</span></span>

<span data-ttu-id="5422b-108">ARG (\* \* *argname* \* *、[* \* *defaultValue* \* \*])</span><span class="sxs-lookup"><span data-stu-id="5422b-108">ARG(\*\* *argName* \*\*,[ \*\* *defaultValue* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5422b-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5422b-109">Parameters</span></span>

|<span data-ttu-id="5422b-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="5422b-110">**Name**</span></span>|<span data-ttu-id="5422b-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5422b-111">**Required/Optional**</span></span>|<span data-ttu-id="5422b-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5422b-112">**Data Type**</span></span>|<span data-ttu-id="5422b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="5422b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5422b-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="5422b-114">_argName_</span></span> <br/> |<span data-ttu-id="5422b-115">必須</span><span class="sxs-lookup"><span data-stu-id="5422b-115">Required</span></span>  <br/> |<span data-ttu-id="5422b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5422b-116">**String**</span></span> <br/> |<span data-ttu-id="5422b-117">呼び出し元のセルが関数に渡すことができる引数の名前です。</span><span class="sxs-lookup"><span data-stu-id="5422b-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="5422b-118">_既定値_</span><span class="sxs-lookup"><span data-stu-id="5422b-118">_default Value_</span></span> <br/> |<span data-ttu-id="5422b-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="5422b-119">Optional</span></span>  <br/> |<span data-ttu-id="5422b-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="5422b-120">**Numeric**</span></span> <br/> |<span data-ttu-id="5422b-121">呼び出し元のセルが_argname_パラメーターの値を渡さなかった場合に、ARG によって返される値です。</span><span class="sxs-lookup"><span data-stu-id="5422b-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5422b-122">注釈</span><span class="sxs-lookup"><span data-stu-id="5422b-122">Remarks</span></span>

<span data-ttu-id="5422b-p103">図形の開発者と同様に、1 つのセルに式を記述し、その式を 1 つまたは複数の別のセルから呼び出すことによって、ユーザー設定関数を作成できます。式には、リテラル文字列、シェイプシートの関数、およびセル参照を入れることができます。また、呼び出し元のセルによって渡される特定の引数を入れることも可能です。</span><span class="sxs-lookup"><span data-stu-id="5422b-p103">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells. The expression can include literal strings, ShapeSheet functions, and cell references. The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="5422b-126">呼び出し元のセルは、ユーザー設定関数を含むセル、およびそのセルが関数に渡す引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5422b-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="5422b-127">式のセルは評価され、結果が呼び出し元のセルに返されます。</span><span class="sxs-lookup"><span data-stu-id="5422b-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="5422b-128">例</span><span class="sxs-lookup"><span data-stu-id="5422b-128">Example</span></span>

<span data-ttu-id="5422b-129">次の例は、3 つの値の集合から中央値を検索するために、EVALCELL 関数と共に ARG 関数を使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5422b-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="5422b-130">式セルに、ユーザー設定関数を定義する次のコードを配置します。</span><span class="sxs-lookup"><span data-stu-id="5422b-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="5422b-131">呼び出しセルに、ユーザー設定関数を呼び出す次のコードを配置します。</span><span class="sxs-lookup"><span data-stu-id="5422b-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


