---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm function [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437414"
---
# <a name="xlsheetnm"></a><span data-ttu-id="ff46d-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="ff46d-104">xlSheetNm</span></span>

<span data-ttu-id="ff46d-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ff46d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ff46d-106">外部参照に含まれる内部シート ID から、ワークシートまたはマクロ シートの名前 (内部参照が渡され場合は、現在のシートの名前) を返します。</span><span class="sxs-lookup"><span data-stu-id="ff46d-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="ff46d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff46d-107">Parameters</span></span>

<span data-ttu-id="ff46d-108">_pxExtref_ (**xltypeRef** または **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="ff46d-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="ff46d-109">名前を取得するシートへの参照。</span><span class="sxs-lookup"><span data-stu-id="ff46d-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="ff46d-110">外部参照 (**xltypeRef**) を渡す場合は、シートの ID のみが含まれているだけで十分です。</span><span class="sxs-lookup"><span data-stu-id="ff46d-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="ff46d-111">ワークシートのセルを表すデータ構造体は無視されるので、指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ff46d-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="ff46d-112">ID が 0 に設定されていると、**xlSheetNm** は現在のシートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="ff46d-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="ff46d-113">内部参照 (**xltypeSef**) を渡すと、**xlSheetNm** は現在のシートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="ff46d-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ff46d-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="ff46d-114">Property value/Return value</span></span>

<span data-ttu-id="ff46d-115">`[Book1]Sheet1` の形式でシートの名前 (**xltypeStr**) を返します。</span><span class="sxs-lookup"><span data-stu-id="ff46d-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="ff46d-116">例</span><span class="sxs-lookup"><span data-stu-id="ff46d-116">Example</span></span>

<span data-ttu-id="ff46d-p102">次の例では、関数の呼び出し元のシートの名前を表示します。この関数は、XLM のコマンド マクロの実行中にマクロ シートから呼び出された場合のみ正常に動作します。その理由は、**xlcAlert** の呼び出しはコマンドでのみ実行可能であり、**xlfCaller** に参照を返させるためには、この関数をダイアログ ボックス、メニュー、コマンド バーからではなく、シートから呼び出さなければならないためです。</span><span class="sxs-lookup"><span data-stu-id="ff46d-p102">The following example displays the name of the sheet from which the function was called. The function works correctly only if called from a macro sheet while executing an XLM command macro. This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ff46d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff46d-120">See also</span></span>

- [<span data-ttu-id="ff46d-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="ff46d-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="ff46d-122">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="ff46d-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

