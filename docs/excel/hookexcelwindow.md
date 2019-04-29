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
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413508"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**ExcelCursorProc** をインストールして、Microsoft Excel のメイン **WndProc** の前に呼び出されるようにします。
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>パラメーター

 _hWndExcel_ (**HANDLE**)
  
Excel のメイン ウィンドウ ハンドル。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は値を返しません。
  
## <a name="remarks"></a>注釈

この関数は、**GetWindowLong()** を使用して Excel **WndProc** のアドレスを取得し、この値をグローバルに保管して、既定の **WndProc** を呼び出したり、復元したりできるようにします。そして最後に、**SetWindowLong()** を使用して、このアドレスを **ExcelCursorProc** のアドレスで置き換えます。
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

