---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid function [excel 2007]
ms.localizationpriority: medium
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34dc592d0f6dae54c73d37bd85d125168d0d9dc1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552158"
---
# <a name="xlsheetid"></a>xlSheetId

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
外部参照を作成するために、名前付きのシートのシート ID を検索します。
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>パラメーター

_pxSheetName_ (**xltypeStr**)
  
(Optional). The name of the book and sheet you want to find out about. If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet. 
  
## <a name="return-value"></a>戻り値

_pxRes-\>val.mref.idSheet_ 内にシート ID を返します。 
  
> [!NOTE]
> _pxRes-\>val.mref.lpmref_ 配列ポインターは、この呼び出しの後で NULL に設定されるため、**xlFree** を呼び出して、このタイプに通常含まれているメモリを解放する必要はありません (これは完全に安全ですが必要ありません)。 
  
## <a name="remarks"></a>注釈

指定されたシートを含むブックは、この関数を使用するために開いている必要があります。DLL から開いていないブックへの参照を作成する方法はありません。**xlSheetId** を使用した参照の作成について詳しくは、「[Excel のメモリ管理](memory-management-in-excel.md)」で **xltypeRef** の作成例を参照してください。 
  
## <a name="example"></a>例

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>関連項目

- [xlSheetNm](xlsheetnm.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

