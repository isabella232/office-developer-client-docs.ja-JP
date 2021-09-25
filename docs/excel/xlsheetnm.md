---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm function [excel 2007]
ms.localizationpriority: medium
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cbc33f6405923de007f19c94a69eb53ed045543c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557541"
---
# <a name="xlsheetnm"></a>xlSheetNm

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
外部参照に含まれる内部シート ID から、ワークシートまたはマクロ シートの名前 (内部参照が渡され場合は、現在のシートの名前) を返します。
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>パラメーター

_pxExtref_ (**xltypeRef** または **xltypeSRef**)
  
名前を取得するシートへの参照。
  
外部参照 (**xltypeRef**) を渡す場合は、シートの ID のみが含まれているだけで十分です。ワークシートのセルを表すデータ構造体は無視されるので、指定する必要はありません。ID が 0 に設定されていると、**xlSheetNm** は現在のシートの名前を返します。 
  
内部参照 (**xltypeSef**) を渡すと、**xlSheetNm** は現在のシートの名前を返します。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

`[Book1]Sheet1` の形式でシートの名前 (**xltypeStr**) を返します。
  
## <a name="example"></a>例

次の例では、関数の呼び出し元のシートの名前を表示します。この関数は、XLM のコマンド マクロの実行中にマクロ シートから呼び出された場合のみ正常に動作します。その理由は、**xlcAlert** の呼び出しはコマンドでのみ実行可能であり、**xlfCaller** に参照を返させるためには、この関数をダイアログ ボックス、メニュー、コマンド バーからではなく、シートから呼び出さなければならないためです。 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>関連項目

- [xlSheetId](xlsheetid.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

