---
title: xlfUnregister (�`�� 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister function [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303893"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="10b73-104">xlfUnregister (形式 1)</span><span class="sxs-lookup"><span data-stu-id="10b73-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="10b73-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="10b73-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="10b73-p101">Microsoft Excel から呼び出された DLL コマンドまたは XLL コマンドから呼び出すことができます。これは、**UNREGISTER** を Excel XLM マクロ シートから呼び出すのと同等です。</span><span class="sxs-lookup"><span data-stu-id="10b73-p101">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel. This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="10b73-108">**xlfUnregister** 関数は、次の 2 つの形式で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="10b73-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="10b73-109">形式 1: 個々のコマンドや関数の登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="10b73-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="10b73-110">形式 2: XLL のアンロードと非アクティブ化を行います。</span><span class="sxs-lookup"><span data-stu-id="10b73-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="10b73-p102">形式 1 で呼び出されると、この関数は、**xlfRegister** または **REGISTER** を使用して既に登録されている DLL 関数またはコマンドの使用カウントを減らします。既に使用カウントが 0 の場合、この関数の効果はありません。DLL 内のすべての関数の使用カウントが 0 になると、DLL はメモリからアンロードされます。</span><span class="sxs-lookup"><span data-stu-id="10b73-p102">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**. If the usage count is already zero, this function has no effect. When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="10b73-p103">**xlfRegister** (形式 1) は、関数またはコマンドの登録 ID ともみなされる非表示名 (関数のテキスト引数 _pxFunctionText_) も定義します。関数の登録を解除する場合は、関数ウィザードにその関数の名前が表示されなくなるように、**xlfSetName** を使用してこの名前を削除する必要があります。詳しくは、「[Excel アドイン (XLL) 開発における既知の問題](known-issues-in-excel-xll-development.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="10b73-p103">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID. When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="10b73-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="10b73-117">Parameters</span></span>

<span data-ttu-id="10b73-118">_pxRegisterId_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="10b73-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="10b73-119">登録を解除する関数の登録 ID。</span><span class="sxs-lookup"><span data-stu-id="10b73-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="10b73-120">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="10b73-120">Property value/Return value</span></span>

<span data-ttu-id="10b73-121">成功した場合は **TRUE** (**xltypeBool**) を返します。それ以外の場合は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="10b73-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="10b73-122">注釈</span><span class="sxs-lookup"><span data-stu-id="10b73-122">Remarks</span></span>

<span data-ttu-id="10b73-p104">関数の登録 ID は、関数の最初の登録時に **xlfRegister** によって返されます。また、[xlfRegisterId 関数](xlfregisterid.md) または [xlfEvaluate 関数](xlfevaluate.md)を呼び出して取得することもできます。関数がまだ登録されていない場合は、xlfRegisterId はその関数を登録しようとすることにご注意ください。このため、単に関数の登録を解除する目的で ID を取得しようとしているのであれば、登録された名前を **xlfEvaluate** に渡して ID を取得することをお勧めします。関数が登録されていない場合、**xlfEvaluate** は #NAME? エラーで失敗します。</span><span class="sxs-lookup"><span data-stu-id="10b73-p104">The registration ID of the function is returned by **xlfRegister** when the function is first registered. It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md). Note that xlfRegisterId tries to register the function if it has not already been registered. For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**. If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="10b73-128">例</span><span class="sxs-lookup"><span data-stu-id="10b73-128">Example</span></span>

<span data-ttu-id="10b73-129">`\SAMPLES\GENERIC\GENERIC.C` の **fExit** 関数のコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="10b73-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a><span data-ttu-id="10b73-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="10b73-130">See also</span></span>

- [<span data-ttu-id="10b73-131">xlfRegister (形式 1)</span><span class="sxs-lookup"><span data-stu-id="10b73-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="10b73-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="10b73-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="10b73-133">xlfUnregister (形式 2)</span><span class="sxs-lookup"><span data-stu-id="10b73-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="10b73-134">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="10b73-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

