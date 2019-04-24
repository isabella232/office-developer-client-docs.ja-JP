---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- tempstr function [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310319"
---
# <a name="tempstr"></a>TempStr

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**xltypeStr** バイト文字列を格納している一時的な **XLOPER** を作成する、非推奨のフレームワーク ライブラリ関数です。入力として、NULL で終了するソース文字列を受け取ります。受け取った文字列の最初の文字を後続の文字列の長さで上書きしようとします。この動作は安全でないことがあり、読み取り専用の文字列を渡すと、Microsoft Excel がクラッシュする可能性があります。 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>パラメーター

 _str_
  
NULL で終了するソース文字列へのポインター。**TempStr** は 255 バイトよりも長い文字列を切り詰めます。 
  
## <a name="return-value"></a>戻り値

渡された文字列バッファーへのポインターを格納している **xltypeStr** 文字列を返します。 
  
## <a name="remarks"></a>注釈

この方法による一時的な文字列の作成は、[TempStrConst と TempStr12](tempstrconst-tempstr12.md) の両方で動作する方法としては推奨されなくなりました。これらの関数は、新しいメモリ バッファーを割り当てて、そのバッファーに渡された文字列をコピーします。**TempStrConst** と **TempStr12** の入力文字列は変更されないため、**const** として宣言されます。これに対して、**TempStr** への入力文字列は変更されるため、**const** として宣言できません。入力文字列の最初の文字は、長さ文字のスペースとして扱われ、この関数によって上書きされます。
  
## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

