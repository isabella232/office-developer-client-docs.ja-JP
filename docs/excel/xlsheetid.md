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
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798989"
---
# <a name="xlsheetid"></a>xlSheetId

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
外部参照を作成するために、名前付きのシートのシート ID を検索します。
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>パラメーター

_pxSheetName_ (**xltypeStr**)
  
(省略可能)。 詳細を確認するブックとシートの名前です。 省略した場合、**xlSheetId** 関数は作業中 (フロント) のシートのシート ID を返します。 
  
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

