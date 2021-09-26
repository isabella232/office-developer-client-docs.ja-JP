---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- tempactiveref function [excel 2007],TempActiveRef12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7faec0ba405c8bb774cf33fc01edb2247fdbea5b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611267"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
作業中のワークシート上にある長方形のブロックのセルへの外部参照を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>パラメーター

 _rwFirst_
  
参照の開始行。
  
 _rwLast_
  
参照の終了行。
  
0 を基準とするため、行 1 は 0 として渡されます。Microsoft Office Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、WORD 整数で使用できる最大値は 65,535 = 2^16 - 1 です。バイトの整数で実行できる最大値とします。ブックを実行する Excel 2007 以降では、最大値は 1,048,575 = 2^20 - 1 です。RW は、XLCALL.H の 32 ビット符号付き整数として定義されます。
  
 _colFirst_
  
参照の開始列番号。
  
 _colLast_
  
参照の終了列番号。
  
列の引数は 0 を基準とするため、列 A は 0 として渡されます。Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、最大値は 255 = 2^8 - 1 です。これは、BYTE 整数で使用できる最大値です。ブックを実行する Excel 2007 では、最大値は 16,383 = 2^14 - 1 です。COL は、XLCALL.H の 32 ビット符号付き整数として定義されます。
  
## <a name="return-value"></a>戻り値

渡される長方形のブロックのセルへの **xltypeRef** 外部参照を返します。 
  
## <a name="example"></a>例

この例では、**TempActiveRef12** 関数を使用して A105:C110 のセルを選択しています。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

