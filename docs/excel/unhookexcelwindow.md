---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- unhookexcelwindow function
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798959"
---
# <a name="unhookexcelwindow"></a><span data-ttu-id="5ce8c-104">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="5ce8c-104">UnhookExcelWindow</span></span>

 <span data-ttu-id="5ce8c-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5ce8c-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5ce8c-p101">以前に **HookExcelWindow** によってインストールされた **ExcelCursorProc** を削除します。この削除操作は、Microsoft Excel のメイン **WndProc** の前に **ExcelCursorProc** を呼び出すために行われている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="5ce8c-p101">Removes the **ExcelCursorProc** that was previously installed by **HookExcelWindow**. This would have been done so that **ExcelCursorProc** was called before the Microsoft Excel main **WndProc**.</span></span>
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a><span data-ttu-id="5ce8c-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ce8c-108">Parameters</span></span>

 <span data-ttu-id="5ce8c-109">_hWndExcel_ (**HANDLE**)</span><span class="sxs-lookup"><span data-stu-id="5ce8c-109">_hWndExcel_ (**HANDLE**)</span></span>
  
<span data-ttu-id="5ce8c-110">Excel のメイン ウィンドウ ハンドル。</span><span class="sxs-lookup"><span data-stu-id="5ce8c-110">The Excel main Windows handle.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5ce8c-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="5ce8c-111">Property Value/Return Value</span></span>

<span data-ttu-id="5ce8c-112">この関数は値を返しません。</span><span class="sxs-lookup"><span data-stu-id="5ce8c-112">The function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ce8c-113">注釈</span><span class="sxs-lookup"><span data-stu-id="5ce8c-113">Remarks</span></span>

<span data-ttu-id="5ce8c-114">この関数は、**SetWindowLong()** を使用して Excel 既定の **WndProc** を復元し、**HookExcelWindow()** によって保存されたアドレスを復元します。</span><span class="sxs-lookup"><span data-stu-id="5ce8c-114">This function restores the Excel default **WndProc** using **SetWindowLong()** to restore the address that was saved by **HookExcelWindow()**.</span></span>
  
### <a name="example"></a><span data-ttu-id="5ce8c-115">例</span><span class="sxs-lookup"><span data-stu-id="5ce8c-115">Example</span></span>

<span data-ttu-id="5ce8c-116">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ce8c-116">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ce8c-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ce8c-117">See also</span></span>



[<span data-ttu-id="5ce8c-118">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="5ce8c-118">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

