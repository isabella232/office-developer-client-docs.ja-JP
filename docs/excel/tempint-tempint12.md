---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12 function [excel 2007],TempInt function [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798952"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
整数を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>パラメーター

 _i_
  
対象の整数値。**XLOPER** 整数は、符号付き 16 ビット整数 (short int) であるのに対し、**XLOPER12** 整数は、符号付き 32 ビット整数 ([long] int) であることにご注意ください。 
  
## <a name="return-value"></a>戻り値

渡された値を含む **xltypeInt** 整数を返します。 
  
## <a name="example"></a>例

この例では、**TempInt12** 関数を使用して、**xlfGetWorkspace** に引数を渡しています。
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

