---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- xlset function [excel 2007]
ms.localizationpriority: medium
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a99d904c4aa9845146ffe2d05dff45859de3b434
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576605"
---
# <a name="xlset"></a>xlSet

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
定数値をセルや範囲にすばやく配置します。詳しくは、「[Excel アドイン (XLL) 開発における既知の問題](known-issues-in-excel-xll-development.md)」の「xlSet と配列数式を含むブック」をご覧ください。
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>パラメーター

_pxReference_ (**xltypeRef** または **xltypeSRef**)
  
A rectangular reference describing the target cell or cells. The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1. 
  
_pxValue_
  
セルに配置される値です。詳しくは、「解説」セクションを参照してください。
  
## <a name="remarks"></a>注釈

### <a name="pxvalue-argument"></a>pxValue 引数

_pxValue_ には、値または配列のいずれかを指定できます。値の場合は、指定の範囲全体にその値が入力されます。配列 (**xltypeMulti**) の場合は、配列の要素が長方形の対応する場所に配置されます。
  
If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle. If you use a vertical array, it is duplicated right to fill the entire rectangle. If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.
  
対象範囲がソース配列よりも小さい場合は、対象範囲の境界まで値がコピーされ、余分なデータは無視されます。
  
指定の長方形の要素を消去する場合は、ソース配列で **xltypeNil** 型の配列要素を使用します。指定の長方形全体を消去するには、2 番目の引数を省略します。 
  
### <a name="restrictions"></a>制限

**xlSet** を元に戻すことはできません。また、以前は使用可能だった、元に戻す操作に関する情報が破棄されます。 
  
**xlSet** では、セルに定数のみを配置でき、数式は配置できません。 
  
**xlSet** は、クラス 3 コマンドと同等の関数として動作します。つまり、DLL がオブジェクト、マクロ、メニュー、ツールバー、ショートカット キー、**[マクロ]** ダイアログ ボックスの **[実行]** ボタン (Excel 2007 以降ではリボンの **[表示]** タブ、以前のバージョンでは **[ツール]** メニューからアクセス可能) から呼び出された場合にのみ DLL で使用できます。 
  
## <a name="example"></a>例

次の例では、マクロから渡された値が B205:B206 に入力されます。このコマンド関数の例には引数が必要であり、**Application.Run** メソッドを使用して、XLM マクロ シートや VBA モジュールから呼び出される場合にのみ動作します。 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a>関連項目

- [xlCoerce](xlcoerce.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

