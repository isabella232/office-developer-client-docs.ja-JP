---
title: Excel インスタンスと メイン ウィンドウ ハンドルへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Excel のハンドルへのアクセス,ハンドル [Excel 2007], アクセス,Excel インスタンス, アクセス,ウィンドウのハンドル [Excel 2007], アクセス
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798897"
---
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="9c075-104">Excel インスタンスと メイン ウィンドウ ハンドルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="9c075-104">How to: Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="9c075-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c075-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9c075-p101">Windows 環境でプログラミングをする場合、Microsoft Excel のインスタンス ハンドルまたはメイン ウィンドウのハンドルの理解が必要になることがあります。たとえば、これらのハンドルは、カスタムの Windows ダイアログ ボックスを作成し、表示するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9c075-p101">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle. For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="9c075-p102">これらのハンドルへのアクセスを提供する 2 つの XLL 専用の C API 関数があります。それぞれに対応する [xlGetInst](xlgetinst.md) 関数と [xlGetHwnd](xlgethwnd.md) 関数です。Win32 では、すべてのハンドルは 32 ビットの整数です。ただし、**XLOPER** が設計されたとき、Windows は 16 ビット システムでした。したがって、構造体は 16 ビット ハンドルのみ可能です。Win32 では、**Excel4** または **Excel4v** で呼び出されたときに、**xlGetInst** 関数と **xlGetHwnd** 関数は、完全な 32 ビット ハンドルの下位部分のみを返します。</span><span class="sxs-lookup"><span data-stu-id="9c075-p102">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively. In Win32, all handles are 32-bit integers. However, when the **XLOPER** was designed, Windows was a 16-bit system. Therefore, the structure only allowed for 16-bit handles. In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="9c075-113">Excel 2007 以降のバージョンでは、[Excel12](excel4-excel12.md) または [Excel12v](excel4v-excel12v.md) でこれらの関数が呼び出されると、返される **XLOPER12** は完全な 32 ビット ハンドルから成っています。</span><span class="sxs-lookup"><span data-stu-id="9c075-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="9c075-p103">完全なインスタンス ハンドルの取得は、どのバージョンの Excel でも容易です。DLL が読み込まれるときに呼び出される Windows コールバック **DllMain** に、完全なインスタンス ハンドルが渡されます。このインスタンス ハンドルをグローバル変数に記録する場合、**xlGetInst** 関数を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9c075-p103">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded. If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="9c075-116">Excel 2003 以前のバージョンでの メイン Excel ハンドルの取得</span><span class="sxs-lookup"><span data-stu-id="9c075-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="9c075-p104">Excel 2003 以前の 32 ビット バージョンのメイン Excel ハンドルを取得するには、まず **xlGetHwnd** 関数を呼び出し、実際のハンドルの下位ワードを取得します。次に、返された下位ワードと一致するものを検索するために、トップレベル ウィンドウの一覧を反復処理する必要があります。次のコードは、その技法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9c075-p104">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle. Then, you must iterate the list of top-level windows to search for a match with the returned low word. The following code illustrates the technique.</span></span> 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord retuned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="9c075-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c075-120">See also</span></span>



[<span data-ttu-id="9c075-121">DLL または XLL ファイルの中からダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="9c075-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="9c075-122">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="9c075-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="9c075-123">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="9c075-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

