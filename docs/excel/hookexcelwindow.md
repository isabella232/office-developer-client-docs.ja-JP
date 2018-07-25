---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- hookexcelwindow function [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798891"
---
# <a name="hookexcelwindow"></a><span data-ttu-id="277f6-104">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="277f6-104">HookExcelWindow</span></span>

 <span data-ttu-id="277f6-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="277f6-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="277f6-106">**ExcelCursorProc** をインストールして、Microsoft Excel のメイン **WndProc** の前に呼び出されるようにします。</span><span class="sxs-lookup"><span data-stu-id="277f6-106">Installs **ExcelCursorProc** so that it is called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="277f6-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="277f6-107">Parameters</span></span>

 <span data-ttu-id="277f6-108">_hWndExcel_ (**HANDLE**)</span><span class="sxs-lookup"><span data-stu-id="277f6-108">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="277f6-109">Excel のメイン ウィンドウ ハンドル。</span><span class="sxs-lookup"><span data-stu-id="277f6-109">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="277f6-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="277f6-110">Property Value/Return Value</span></span>

<span data-ttu-id="277f6-111">この関数は値を返しません。</span><span class="sxs-lookup"><span data-stu-id="277f6-111">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="277f6-112">注釈</span><span class="sxs-lookup"><span data-stu-id="277f6-112">Remarks</span></span>

<span data-ttu-id="277f6-p101">この関数は、**GetWindowLong()** を使用して Excel **WndProc** のアドレスを取得し、この値をグローバルに保管して、既定の **WndProc** を呼び出したり、復元したりできるようにします。そして最後に、**SetWindowLong()** を使用して、このアドレスを **ExcelCursorProc** のアドレスで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="277f6-p101">The function obtains the address of the Excel **WndProc** through the use of **GetWindowLong()**. It stores this value in a global that can be used to call the default **WndProc** and also to restore it. Finally, it replaces this address with the address of **ExcelCursorProc** using **SetWindowLong()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="277f6-116">例</span><span class="sxs-lookup"><span data-stu-id="277f6-116">Example</span></span>

<span data-ttu-id="277f6-117">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="277f6-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="277f6-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="277f6-118">See also</span></span>



[<span data-ttu-id="277f6-119">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="277f6-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

