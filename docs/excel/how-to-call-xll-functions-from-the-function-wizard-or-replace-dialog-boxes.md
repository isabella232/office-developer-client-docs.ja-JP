---
title: 関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xll functions [excel 2007], calling from replace dialog box,Replace dialog box [Excel 2007], calling XLL functions,Function Wizard [Excel 2007], calling XLL functions,XLL functions [Excel 2007], calling from Function Wizard
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410750"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="d1618-104">関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="d1618-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="d1618-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d1618-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d1618-p101">多くの場合、Microsoft Excel はブック (計算がマクロの制御下にある場合はブックの一部) の通常の再計算中に XLL 関数を呼び出します。関数は名前付き範囲や条件付き書式設定式に含まれていることがあり、セルの数式には存在しないことがある点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="d1618-p101">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro. Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="d1618-p102">There are two circumstances where a function can be called from an Excel dialog box. One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time. The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box. For the **Paste Function Arguments** dialog box, you might not want your function to execute normally. This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span><span class="sxs-lookup"><span data-stu-id="d1618-p102">There are two circumstances where a function can be called from an Excel dialog box. One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time. The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box. For the **Paste Function Arguments** dialog box, you might not want your function to execute normally. This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="d1618-p103">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number. Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type. It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span><span class="sxs-lookup"><span data-stu-id="d1618-p103">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number. Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type. It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="d1618-116">コールバック関数は、次の手順でのみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1618-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="d1618-117">このウィンドウの親が Excel の現在のインスタンスであることを確認します (実行中のインスタンスが複数ある場合)。</span><span class="sxs-lookup"><span data-stu-id="d1618-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="d1618-118">Windows によって渡されたハンドルからクラス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d1618-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="d1618-119">クラス名が **bosa_sdm_XL**n の形式であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1618-119">Check if the class name is of the form **bosa_sdm_XL**n.</span></span>
    
4. <span data-ttu-id="d1618-p104">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text. The window title is obtained using the Windows API call **GetWindowText**.</span><span class="sxs-lookup"><span data-stu-id="d1618-p104">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text. The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="d1618-p105">次の C++ コードは、Windows に渡されるクラスとコールバックを示しています (上記の手順を実行します)。これは、該当するダイアログ ボックスのどちらかに専用のテストを呼び出す関数から呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1618-p105">The following C++ code shows a class and callback to be passed to Windows that performs these steps. This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d1618-p106">将来の Excel のバージョンのウィンドウ タイトルは変更される可能性があり、このコードが無効になることがあります。また、**window_title_text** を **NULL** に設定すると、コールバックの検索でウィンドウ タイトルを無視するという効果が得られます。</span><span class="sxs-lookup"><span data-stu-id="d1618-p106">Window titles of future Excel versions might change and invalidate this code. Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

<span data-ttu-id="d1618-126">**[関数の貼り付け]** ダイアログ ボックスにはタイトルがありません。そのため、次に示す関数では、タイトルのないウィンドウという一致条件を表すために、タイトル検索の文字列に空の文字列である "" をコールバック関数に渡しています。</span><span class="sxs-lookup"><span data-stu-id="d1618-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a><span data-ttu-id="d1618-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1618-127">See also</span></span>



[<span data-ttu-id="d1618-128">Excel での XLL コードへのアクセス</span><span class="sxs-lookup"><span data-stu-id="d1618-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="d1618-129">DLL または XLL から Excel に呼び出す</span><span class="sxs-lookup"><span data-stu-id="d1618-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="d1618-130">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="d1618-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

