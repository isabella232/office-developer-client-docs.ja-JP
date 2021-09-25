---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- tempactivecolumn12 function [excel 2007],TempActiveColumn function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0ab26134edca76e026f2fe46c3b111e917a7dad1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614592"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
作業中のシートの列全体の外部参照を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>パラメーター

 _col_ (**BYTE**)
  
参照する列。0 を基準とするため、列 A は 0 として渡されます。Microsoft Office Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、BYTE 整数で使用できる最大値は 255 = 2^8 - 1 です。バイトの整数で実行できる最大値とします。ブックを実行する Excel 2007 では、最大値は 16,383 = 2^14 - 1 です。COL は、XLCALL.H の 32 ビット符号付き整数として定義されます。
  
## <a name="return-value"></a>戻り値

渡される列の **xltypeRef** 外部参照を返します。 
  
## <a name="example"></a>例

次の例では、**TempActiveColumn12** を使用して、列 B 全体を選択します。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

