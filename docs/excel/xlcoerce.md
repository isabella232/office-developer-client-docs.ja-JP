---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- xlcoerce function [excel 2007]
ms.localizationpriority: medium
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e02020b6afe67e9c1035e63866c2dd9bff0b24c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621347"
---
# <a name="xlcoerce"></a>xlCoerce

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**XLOPER**/ **XLOPER12** の型を別の型に変換するか、シートのセルの値を検索します。 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>パラメーター

 _pxSource_
  
変換対象のソース **XLOPER**/ **XLOPER12**。 
  
 _pxDestType_ (**xltypeInt**)
  
(Optional). A bit-mask of the resulting types you are willing to accept. You should use the bitwise **OR** operator ( | ) to specify multiple possible types. If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**. This makes **xlCoerce** the most convenient way to look up cell values. 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

強制変換された値 (**xltypeStr**、**xltypeNum**、**xltypeBool**、**xltypeErr**、**xltypeNil**、または **xltypeMulti**) を返します。
  
## <a name="remarks"></a>注釈

 **xlCoerce** は **xltypeBigData** または **xltypeFlow** に変換できず、その逆の変換もできません。**xltypeMissing** または **xltypeNil** の型を _pxDestType_ として渡すことは、引数を省略することに相当します。たとえば、文字列には数字に変換でないものがあります。 
  
配列または複数セルの参照を単一値の型に変換すると、結果は一番上の左のセルまたは配列の要素の値になります。
  
## <a name="example"></a>例

次のコードは、`\SAMPLES\EXAMPLE\EXAMPLE.C` にあります。 
  
> [!NOTE]
> ここに示される強制手順が削除され、**xInt** が直接 **xlcAlert** に渡されるように、**XlcAlert** 関数は暗黙的に引数を文字列に変換しようとします。**xlcAlert** はコマンドのマクロであるため、このコードはマクロ シートから呼び出されたときのみ正しく作動します。 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a>関連項目



[xlSet](xlset.md)


[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

