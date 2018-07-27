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
# <a name="access-excel-instance-and-main-window-handles"></a>Excel インスタンスと メイン ウィンドウ ハンドルへのアクセス

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Windows 環境でプログラミングをする場合、Microsoft Excel のインスタンス ハンドルまたはメイン ウィンドウのハンドルの理解が必要になることがあります。たとえば、これらのハンドルは、カスタムの Windows ダイアログ ボックスを作成し、表示するのに役立ちます。
  
これらのハンドルへのアクセスを提供する 2 つの XLL 専用の C API 関数があります。それぞれに対応する [xlGetInst](xlgetinst.md) 関数と [xlGetHwnd](xlgethwnd.md) 関数です。Win32 では、すべてのハンドルは 32 ビットの整数です。ただし、**XLOPER** が設計されたとき、Windows は 16 ビット システムでした。したがって、構造体は 16 ビット ハンドルのみ可能です。Win32 では、**Excel4** または **Excel4v** で呼び出されたときに、**xlGetInst** 関数と **xlGetHwnd** 関数は、完全な 32 ビット ハンドルの下位部分のみを返します。 
  
Excel 2007 以降のバージョンでは、[Excel12](excel4-excel12.md) または [Excel12v](excel4v-excel12v.md) でこれらの関数が呼び出されると、返される **XLOPER12** は完全な 32 ビット ハンドルから成っています。 
  
完全なインスタンス ハンドルの取得は、どのバージョンの Excel でも容易です。DLL が読み込まれるときに呼び出される Windows コールバック **DllMain** に、完全なインスタンス ハンドルが渡されます。このインスタンス ハンドルをグローバル変数に記録する場合、**xlGetInst** 関数を呼び出す必要はありません。 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Excel 2003 以前のバージョンでの メイン Excel ハンドルの取得

Excel 2003 以前の 32 ビット バージョンのメイン Excel ハンドルを取得するには、まず **xlGetHwnd** 関数を呼び出し、実際のハンドルの下位ワードを取得します。次に、返された下位ワードと一致するものを検索するために、トップレベル ウィンドウの一覧を反復処理する必要があります。次のコードは、その技法を示しています。 
  
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

## <a name="see-also"></a>関連項目



[DLL または XLL ファイルの中からダイアログ ボックスを表示する](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Excel XLL の開発](developing-excel-xlls.md)

