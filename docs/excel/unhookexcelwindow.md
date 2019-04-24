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
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310312"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
以前に **HookExcelWindow** によってインストールされた **ExcelCursorProc** を削除します。この削除操作は、Microsoft Excel のメイン **WndProc** の前に **ExcelCursorProc** を呼び出すために行われている場合もあります。
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>パラメーター

 _hWndExcel_ (**HANDLE**)
  
Excel のメイン ウィンドウ ハンドル。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は値を返しません。
  
## <a name="remarks"></a>注釈

この関数は、**SetWindowLong()** を使用して Excel 既定の **WndProc** を復元し、**HookExcelWindow()** によって保存されたアドレスを復元します。
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

