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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304096"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
When a modal dialog box is displayed over the Microsoft Excel window, the cursor is a busy cursor over the Excel window. This **WndProc** traps WM_SETCURSOR type Windows messages and changes the cursor back to a normal arrow. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>パラメーター

 _hWndDlg_ (**HWND**)
  
ダイアログ ボックスの HWND Windows ハンドルを含んでいます。
  
 _message_ (**UINT**)
  
応答メッセージ
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Windows より渡される引数
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

LRESULT: メッセージがハンドルされた場合は 0、それ以外の場合は、既定の **WndProc** から返される結果。
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

