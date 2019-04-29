---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid function [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420060"
---
# <a name="xlfregisterid"></a><span data-ttu-id="532bd-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="532bd-104">xlfRegisterId</span></span>

<span data-ttu-id="532bd-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="532bd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="532bd-p101">Microsoft Excel から呼び出された DLL コマンドから呼び出すことができます。関数が既に登録されている場合は、その関数を再登録しないで、関数の既存の登録 ID を返します。関数がまだ登録されていない場合は、その関数を登録して、登録 ID を返します。</span><span class="sxs-lookup"><span data-stu-id="532bd-p101">Can be called from a DLL that has itself been called by Microsoft Excel. If a function is already registered, it returns the existing register ID for that function without reregistering it. If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="532bd-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="532bd-109">Parameters</span></span>

<span data-ttu-id="532bd-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="532bd-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="532bd-111">関数が含まれている DLL の名前。</span><span class="sxs-lookup"><span data-stu-id="532bd-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="532bd-112">_pxProcedure_ (**xltypeStr** または **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="532bd-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="532bd-p102">文字列の場合は、呼び出す関数の名前です。数字の場合は、呼び出す関数のエクスポートの順序番号です。明確で堅牢にするために、常に文字列形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="532bd-p102">If a string, the name of the function to call. If a number, the ordinal export number of the function to call. For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="532bd-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="532bd-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="532bd-p103">関数へのすべての引数の型と関数の戻り値の型を指定する、省略可能な文字列。詳しくは、「解説」セクションを参照してください。**xlAutoRegister** を定義するスタンドアロン DLL (XLL) では、この引数を省略できます。</span><span class="sxs-lookup"><span data-stu-id="532bd-p103">An optional string specifying the types of all the arguments to the function and the type of the return value of the function. For more information, see the "Remarks" section. This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="532bd-120">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="532bd-120">Property value/Return value</span></span>

<span data-ttu-id="532bd-121">後続の **xlfUnregister** への呼び出しに使用できる、関数 (**xltypeNum**) の登録 ID を返します。</span><span class="sxs-lookup"><span data-stu-id="532bd-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="532bd-122">注釈</span><span class="sxs-lookup"><span data-stu-id="532bd-122">Remarks</span></span>

<span data-ttu-id="532bd-p104">登録 ID は後で登録解除する際に必要になるが、維持のために気を使いたくない、という場合に、この関数が役立ちます。また、割り当てる関数が DLL にある場合は、メニュー、ツール、およびボタンへの割り当てにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="532bd-p104">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering. It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="532bd-125">**xlfRegister** に指定された有効な _pxFunctionText_ 引数を使用して DLL または XLL 関数が登録されている場合は、関数 **xlfEvaluate** に _pxFunctionText_ を渡すことで、その登録 ID を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="532bd-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="532bd-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="532bd-126">See also</span></span>

- [<span data-ttu-id="532bd-127">REGISTER</span><span class="sxs-lookup"><span data-stu-id="532bd-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="532bd-128">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="532bd-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="532bd-129">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="532bd-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

