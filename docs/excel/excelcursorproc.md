---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc function [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432493"
---
# <a name="excelcursorproc"></a><span data-ttu-id="9a338-104">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="9a338-104">ExcelCursorProc</span></span>

 <span data-ttu-id="9a338-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9a338-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9a338-p101">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window. This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span><span class="sxs-lookup"><span data-stu-id="9a338-p101">When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window. This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow.</span></span> 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a><span data-ttu-id="9a338-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9a338-108">Parameters</span></span>

 <span data-ttu-id="9a338-109">_hWndDlg_ (**HWND**)</span><span class="sxs-lookup"><span data-stu-id="9a338-109">_hWndDlg_ (**HWND**)</span></span>
  
<span data-ttu-id="9a338-110">ダイアログ ボックスの HWND Windows ハンドルを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="9a338-110">Contains the HWND Windows handle of the dialog box.</span></span>
  
 <span data-ttu-id="9a338-111">_message_ (**UINT**)</span><span class="sxs-lookup"><span data-stu-id="9a338-111">_message_ (**UINT**)</span></span>
  
<span data-ttu-id="9a338-112">応答メッセージ</span><span class="sxs-lookup"><span data-stu-id="9a338-112">The message to respond to.</span></span>
  
 <span data-ttu-id="9a338-113">_wParam_ (**WPARAM**)</span><span class="sxs-lookup"><span data-stu-id="9a338-113">_wParam_ (**WPARAM**)</span></span>
  
 <span data-ttu-id="9a338-114">_lParam_ (**LPARAM**)</span><span class="sxs-lookup"><span data-stu-id="9a338-114">_lParam_ (**LPARAM**)</span></span>
  
<span data-ttu-id="9a338-115">Windows より渡される引数</span><span class="sxs-lookup"><span data-stu-id="9a338-115">Arguments passed by Windows.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9a338-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="9a338-116">Property value/Return value</span></span>

<span data-ttu-id="9a338-117">LRESULT: メッセージがハンドルされた場合は 0、それ以外の場合は、既定の **WndProc** から返される結果。</span><span class="sxs-lookup"><span data-stu-id="9a338-117">LRESULT: 0 if the message was handled, otherwise the result returned by the default **WndProc**.</span></span>
  
### <a name="example"></a><span data-ttu-id="9a338-118">例</span><span class="sxs-lookup"><span data-stu-id="9a338-118">Example</span></span>

<span data-ttu-id="9a338-119">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a338-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a338-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a338-120">See also</span></span>



[<span data-ttu-id="9a338-121">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="9a338-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

