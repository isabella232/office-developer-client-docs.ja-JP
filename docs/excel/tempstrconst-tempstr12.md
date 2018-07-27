---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- tempstr12 function [excel 2007],TempStrConst function [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798958"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**xltypeStr** 文字列を含む一時的な **XLOPER/XLOPER12** を作成するフレームワーク ライブラリ関数。入力として Null で終了するソースの文字列を受け取ります。この関数は、新しいメモリ バッファーを割り当てて、そのバッファーに渡された文字列をコピーします。入力文字列は変更されないため、**const** として宣言されます。
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>パラメーター

 _str_
  
Null で終了するソースの文字列へのポインター。**XLOPER** の場合、TempStrConst は 255 バイトより長い文字列を切り捨てます。**XLOPER12** の場合、TempStr12Const は 32,767 Unicode 文字より長い文字列を切り捨てます。
  
## <a name="return-value"></a>戻り値

渡された文字列バッファーのコピーを格納している **xltypeStr** 文字列を返します。 
  
## <a name="remarks"></a>注釈

**XLOPER** 文字列のフレームワーク関数 **TempStr** の動作は異なります。指定された文字列の最初の文字を後続の文字列の長さで上書きしようとするため、注意が必要です。この動作は安全でないことがあり、読み取り専用の文字列を渡すと、Microsoft Excel がクラッシュする可能性があります。この方法による一時的な文字列の作成は、**TempStrConst** と **TempStr12** の両方で動作する方法としては推奨されなくなりました。したがって、入力文字列の最初の文字は、文字列の先頭として (つまり、長さを表す文字または長さを表す文字用のスペースとしてではなく) 処理されます。影響が予測できないため、開始時にエンコードされた長さを表す文字のある文字列は渡さないでください。 
  
## <a name="example"></a>例

この例では、**TempStr12** 関数を使用してメッセージ ボックスの文字列を作成します。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

