---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- temperr function [excel 2007],TempErr12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310347"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ワークシートのエラーを含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>パラメーター

 _err_
  
目的のエラー コードまたはリテラル数値と同等の数値を次の表に示します。
  
|**エラー**|**XLCALL.H で定義されたエラー コード**|**同等の 10 進数**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |.0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7  <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |約  <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |最高  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>戻り値

渡されたエラー コードを含む **xltypeBool** を返します。 
  
## <a name="example"></a>例

この例では、**TempErr12** 関数を使用して #VALUE! エラーを Excel に返します。 
  
> [!NOTE]
> フレームワーク ライブラリ関数 **TempErr12** は、内部バッファーからメモリを割り当てます。割り当てられたメモリは通常、フレームワーク関数 **Excel12f** が呼び出されると解放されます。**Excel12f** を呼び出さずに、この例の関数を繰り返し呼び出すと、メモリ リークが発生します。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

