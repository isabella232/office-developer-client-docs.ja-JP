---
title: フレームワーク ライブラリの関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- framework library functions [excel 2007],functions [Excel 2007], Framework library
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798893"
---
# <a name="functions-in-the-framework-library"></a>フレームワーク ライブラリの関数

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
フレームワーク ライブラリは、XLL を簡単に記述できるようにするために作成されました。 これには、**XLOPER**/ **XLOPER12** メモリの管理、一時 **XLOPER**/ **XLOPER12** の作成、Microsoft Excel のコールバック関数の確実な呼び出し (**Excel4**、**Excel4v**、** Excel12 **、** Excel12v **)、接続されている端末上のデバッグ文字列の印刷のための単純な関数が含まれています。
  
このライブラリに含まれている関数は、次のようなコードの一部を簡略化するのに役立ちます。
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

簡略化されたコードは次の例のようになります。
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

次の関数がフレームワーク ライブラリに含まれています。
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**XLOPER で使用する関数**|**XLOPER12 で使用する関数**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[TempErr](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
これらの関数を使用すると、DLL または XLL を記述するために必要な時間を短くできます。また、サンプル アプリケーション GENERIC から開発を開始しても開発時間を短縮できます。GENERIC.C をテンプレートとして使用して、XLL のフレームワークをセットアップしてから、既存のコードを独自のコードに置き換えることができます。
  
一時 **XLOPER**/ **XLOPER12** 関数は、フレームワーク ライブラリで管理されるローカル ヒープのメモリを使って **XLOPER**/ **XLOPER12** の値を作成します。**XLOPER**/ **XLOPER12** の値は、**FreeAllTempMemory** 関数を呼び出すまで、あるいは **Excel** または **Excel12f** 関数を呼び出すまで、有効です (**Excel** 関数と **Excel12f** 関数は、すべての一時メモリを解放してから戻ります)。 
  
フレームワーク ライブラリの関数を使用するには、FRAMEWRK.H ファイルを C コードに含め、FRAMEWRK.C ファイルまたは FRMWRK32.LIB ファイルをコード プロジェクトに追加する必要があります。
  
## <a name="see-also"></a>関連項目

- [Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)

