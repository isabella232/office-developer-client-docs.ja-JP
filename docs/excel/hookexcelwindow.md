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
ms.localizationpriority: medium
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ded29045ae66d4f4a73b68bc74d695ca8059449
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576710"
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

