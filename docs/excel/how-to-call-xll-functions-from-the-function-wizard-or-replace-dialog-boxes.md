---
title: 関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xll functions [excel 2007], calling from replace dialog box,Replace dialog box [Excel 2007], calling XLL functions,Function Wizard [Excel 2007], calling XLL functions,XLL functions [Excel 2007], calling from Function Wizard
ms.localizationpriority: medium
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3709c3f4736a5eb977bbfdd6f13a1fd9b87f1d7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592978"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
多くの場合、Microsoft Excel はブック (計算がマクロの制御下にある場合はブックの一部) の通常の再計算中に XLL 関数を呼び出します。関数は名前付き範囲や条件付き書式設定式に含まれていることがあり、セルの数式には存在しないことがある点に注意してください。
  
There are two circumstances where a function can be called from an Excel dialog box. One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time. The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box. For the **Paste Function Arguments** dialog box, you might not want your function to execute normally. This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box. 
  
Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL** n, where n is a number. Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type. It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.
  
コールバック関数は、次の手順でのみ実行する必要があります。
  
1. このウィンドウの親が Excel の現在のインスタンスであることを確認します (実行中のインスタンスが複数ある場合)。
    
2. Windows によって渡されたハンドルからクラス名を取得します。
    
3. クラス名が **bosa_sdm_XL** n の形式であることを確認します。
    
4. If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text. The window title is obtained using the Windows API call **GetWindowText**.
    
次の C++ コードは、Windows に渡されるクラスとコールバックを示しています (上記の手順を実行します)。これは、該当するダイアログ ボックスのどちらかに専用のテストを呼び出す関数から呼び出します。 
  
> [!NOTE]
> 将来の Excel のバージョンのウィンドウ タイトルは変更される可能性があり、このコードが無効になることがあります。また、**window_title_text** を **NULL** に設定すると、コールバックの検索でウィンドウ タイトルを無視するという効果が得られます。 
  
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

**[関数の貼り付け]** ダイアログ ボックスにはタイトルがありません。そのため、次に示す関数では、タイトルのないウィンドウという一致条件を表すために、タイトル検索の文字列に空の文字列である "" をコールバック関数に渡しています。 
  
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

## <a name="see-also"></a>関連項目



[Excel での XLL コードへのアクセス](accessing-xll-code-in-excel.md)
  
[DLL または XLL から Excel に呼び出す](calling-into-excel-from-the-dll-or-xll.md)
  
[Excel XLL の開発](developing-excel-xlls.md)

