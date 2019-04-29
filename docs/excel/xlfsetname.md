---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfsetname function [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404261"
---
# <a name="xlfsetname"></a><span data-ttu-id="2304d-104">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="2304d-104">xlfSetName</span></span>

<span data-ttu-id="2304d-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2304d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2304d-106">DLL に関連付けられている定義済みの名前を作成および削除するために使用します。</span><span class="sxs-lookup"><span data-stu-id="2304d-106">Used to create and delete defined names associated with the DLL.</span></span>
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a><span data-ttu-id="2304d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2304d-107">Parameters</span></span>

<span data-ttu-id="2304d-108">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="2304d-108">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="2304d-109">名前の範囲。この名前は、有効な名前に関する Microsoft Excel の通常の制限に準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2304d-109">The name of the range, which should conform to the usual limitations in Microsoft Excel on valid names.</span></span>
  
<span data-ttu-id="2304d-110">_pxNameDefinition_ (**xltypeStr**、**xltypeNum**、**xltypeBool**、**xltypeErr**、**xltypeMulti**、**xltypeSRef**、**xltypeRef**、または **xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="2304d-110">_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**, or **xltypeInt**)</span></span>
  
<span data-ttu-id="2304d-111">(省略可能)。</span><span class="sxs-lookup"><span data-stu-id="2304d-111">(Optional).</span></span> <span data-ttu-id="2304d-112">値、値のセット、セル、または _pxNameText_ として定義されたセルの範囲。</span><span class="sxs-lookup"><span data-stu-id="2304d-112">The value, set of values, cell, or range of cells that  _pxNameText_ is defined as.</span></span> <span data-ttu-id="2304d-113">省略した場合は名前が削除されます。</span><span class="sxs-lookup"><span data-stu-id="2304d-113">If omitted, the name is deleted.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2304d-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="2304d-114">Property value/Return value</span></span>

<span data-ttu-id="2304d-115">_pxRes _ (**xltypeBool** または **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="2304d-115">_pxRes_ (**xltypeBool** or **xltypeErr**)</span></span>
  
<span data-ttu-id="2304d-p102">操作が成功した場合は TRUE、名前を作成または削除できなかった場合は FALSE を返します。引数の 1 つ以上が無効であれば、#VALUE! を返します。</span><span class="sxs-lookup"><span data-stu-id="2304d-p102">TRUE if the operation succeeded or FALSE if the name could not be created or deleted. Returns #VALUE! if one or more of the arguments was invalid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2304d-119">注釈</span><span class="sxs-lookup"><span data-stu-id="2304d-119">Remarks</span></span>

<span data-ttu-id="2304d-p103">有効な _pxFunctionText_ 引数を設定した **xlfRegister** を使用して関数またはコマンドが登録されると、Excel は DLL リソースに関連付けた名前を作成します。DLL がアンロードされる場合、これらの名前は [xlfSetName 関数](xlfsetname.md)を使用して削除されなければなりません。ただし、この削除操作は Excel の既知の問題が原因で失敗します。詳細については、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2304d-p103">When a function or command is registered using **xlfRegister** with a valid  _pxFunctionText_ argument, Excel creates a name associated with the DLL resource. When your DLL is being unloaded, such names should be deleted using the [xlfSetName function](xlfsetname.md). However, due to a known issue in Excel, this deletion operation fails. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
### <a name="example"></a><span data-ttu-id="2304d-124">例</span><span class="sxs-lookup"><span data-stu-id="2304d-124">Example</span></span>

<span data-ttu-id="2304d-125">`\SAMPLES\GENERIC\GENERIC.C` で、**xlAutoClose** 関数のコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2304d-125">See the code for the **xlAutoClose** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2304d-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="2304d-126">See also</span></span>

- [<span data-ttu-id="2304d-127">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="2304d-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

