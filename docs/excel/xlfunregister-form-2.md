---
title: xlfUnregister (形式 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798996"
---
# <a name="xlfunregister-form-2"></a><span data-ttu-id="9dee1-104">xlfUnregister (形式 2)</span><span class="sxs-lookup"><span data-stu-id="9dee1-104">xlfUnregister (Form 2)</span></span>

<span data-ttu-id="9dee1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9dee1-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9dee1-p101">Microsoft Excel から呼び出された DLL コマンドまたは XLL コマンドから呼び出すことができます。これは、**UNREGISTER** を Excel XLM マクロ シートから呼び出すのと同等です。</span><span class="sxs-lookup"><span data-stu-id="9dee1-p101">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel. This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="9dee1-108">**xlfUnregister** 関数は、次の 2 つの形式で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="9dee1-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="9dee1-109">形式 1: 個々のコマンドや関数の登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="9dee1-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="9dee1-110">形式 2: XLL のアンロードと非アクティブ化を行います。</span><span class="sxs-lookup"><span data-stu-id="9dee1-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="9dee1-p102">形式 2 で呼び出されると、この関数は DLL やコード リソースの完全なアンロードを強制します。別のマクロで現在使われていても、DLL 内のすべての関数の登録を解除します。関数の使用について考慮されません。この関数は **xlAutoClose** を呼び出してから、DLL 内のすべての関数の登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="9dee1-p102">Called in Form 2, this function forces a DLL or code resource to be unloaded completely. It unregisters all of the functions in a DLL, even if they are currently in use by another macro, no matter what the use count. This function calls **xlAutoClose**, and then unregisters all the functions in the DLL.</span></span>
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="9dee1-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9dee1-114">Parameters</span></span>

<span data-ttu-id="9dee1-115">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="9dee1-115">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="9dee1-116">DLL の名前。</span><span class="sxs-lookup"><span data-stu-id="9dee1-116">The name of the DLL.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9dee1-117">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="9dee1-117">Property Value/Return Value</span></span>

<span data-ttu-id="9dee1-118">成功した場合、**TRUE** (**xltypeBool**) を返します。</span><span class="sxs-lookup"><span data-stu-id="9dee1-118">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="9dee1-119">失敗した場合は、**FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="9dee1-119">If successful, returns **TRUE** (xltypeBool). If unsuccessful, returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9dee1-120">注釈</span><span class="sxs-lookup"><span data-stu-id="9dee1-120">Remarks</span></span>

> [!NOTE] 
> <span data-ttu-id="9dee1-121">この形式の関数を [xlAutoClose](xlautoclose.md) の実装から呼び出して、1 つの単純な関数の呼び出しにより DLL のすべてのリソースの登録を解除しようとしないでください。</span><span class="sxs-lookup"><span data-stu-id="9dee1-121">Note: Do not call this form of the function from your implementation of the [xlAutoClose](xlautoclose.md) in an attempt to unregister all of the DLL's resources with one simple function call. This leads to recursive calling of xlAutoClose and a stack overflow.</span></span> <span data-ttu-id="9dee1-122">これにより、**xlAutoClose** の再帰呼び出しがなされスタック オーバーフローになります。</span><span class="sxs-lookup"><span data-stu-id="9dee1-122">This leads to recursive calling of **xlAutoClose** and a stack overflow.</span></span> 
  
### <a name="remember-to-delete-names"></a><span data-ttu-id="9dee1-123">名前を削除することを忘れないでください</span><span class="sxs-lookup"><span data-stu-id="9dee1-123">Remember to Delete Names</span></span>

<span data-ttu-id="9dee1-p105">_pxFunctionText_ 引数を **xlfRegister** に指定する場合は、DLL の関数とコマンドの登録時に、それぞれについて 2 つ目の引数を省略して **xlfSetName** を呼び出し、関数が関数ウィザードに表示されないように名前を明示的に削除する必要があります。詳細については、「[Excel アドイン (XLL) 開発における既知の問題](known-issues-in-excel-xll-development.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9dee1-p105">If you specified the  _pxFunctionText_ argument to **xlfRegister**, when registering the DLL's functions and commands, you must explicitly delete the names by calling **xlfSetName** for each one, omitting the second argument so that the function no longer appears in the Function Wizard. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9dee1-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="9dee1-126">See also</span></span>

- [<span data-ttu-id="9dee1-127">xlfRegister (形式 1)</span><span class="sxs-lookup"><span data-stu-id="9dee1-127">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="9dee1-128">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="9dee1-128">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="9dee1-129">xlfUnregister (形式 1)</span><span class="sxs-lookup"><span data-stu-id="9dee1-129">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="9dee1-130">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="9dee1-130">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

