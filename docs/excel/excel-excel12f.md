---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- excel function [excel 2007],Excel12f function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bae0e56648392469dd532259c941e71674f67fd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601367"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework library functions. **Excel** is a wrapper for the [Excel4](excel4-excel12.md) function. **Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function. Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed. If an error occurs, each prints a debug message. When finished, each frees all temporary memory that might have been created for temporary **XLOPER** s and **XLOPER12** s.
  
 **Excel12f** から Excel 2007 C API ライブラリ以降の DLL からのみ呼び出すことができます。さらに、Excel 2007 以降で起動したときのみ動作し、それ以外は **xlretFailed** で失敗します。 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>パラメーター

 _iFunction_ (**int**)
  
呼び出すコマンドまたは関数を示す数値。詳細については、「[Excel4/Excel12](excel4-excel12.md)」を参照してください。
  
 _pxRes_
  
評価された関数の結果のポインター。結果に示されるメモリはすべて、Excel によって割り当てられ、不要になったら [xlFree](xlfree.md) を呼び出して解放するか、または Excel に戻す場合は **xlbitXLFree** を設定して解放します。 
  
 _iCount_ (**int**)
  
関数に渡される引数の数。Excel 2007 以降、引数の数は 255 に制限されています。それ以前のバージョンでは引数の数は 30 に制限されています。
  
 _argument1, ..._
  
省略可能な、関数の引数。すべての引数は、**Excel** の場合は **XLOPER** へのポインター、**Excel12f** の場合は **XLOPER12** へのポインターにする必要があります。
  
## <a name="return-value"></a>戻り値

Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**. See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes. In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected. 
  
## <a name="example"></a>例

この例では、不正な引数を **Excel12f** 関数に渡して、デバッガーにメッセージを送信しています。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>関連項目



[Excel4/Excel12](excel4-excel12.md)


[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

