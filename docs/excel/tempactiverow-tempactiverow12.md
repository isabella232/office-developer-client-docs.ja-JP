---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- tempactiverow function [excel 2007],TempActiveRow12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798942"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
作業中のシートの行全体の外部参照を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>パラメーター

 _row_
  
参照する行。0 を基準とするため、行 1 は 0 として渡されます。Microsoft Office Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、WORD 整数で使用できる最大値は 65,535 = 2^16 - 1 です。バイトの整数で実行できる最大値とします。ブックを実行する Excel 2007 以降では、最大値は 1,048,575 = 2^20 - 1 です。RW は、XLCALL.H の 32 ビット符号付き整数として定義されます。
  
## <a name="return-value"></a>戻り値

渡される行のセルの **xltypeRef** 外部参照が返されます。 
  
## <a name="example"></a>例

この例では、**TempActiveRow12** 関数を使用して行 113 を選択します。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

