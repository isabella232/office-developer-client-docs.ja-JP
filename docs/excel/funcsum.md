---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum function [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406942"
---
# <a name="funcsum"></a>FuncSum

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
1 ～ 29 個の引数を取って、それらの合計を計算する、サンプル ユーザー定義ワークシート関数。各引数に指定できるのは、1 つの数字、範囲、または配列です。GENERIC.xll が読み込まれると、GENERIC.xll によってこの関数が登録されて、ワークシートから呼び出すことができるようになります。 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>パラメーター

 _px1-px29_ (**LPXLOPER12**)
  
**XLOPER12** 引数へのポインター。この関数は、任意の入力の型を受け入れますが、数字、数字のリテラル配列、および数字または空白セルのみが含まれている範囲を対象に作動するようコーディングされています。指定された引数の数が 29 に満たない場合、残りの引数は **xltypeMissing** として指定されます。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

(**LPXLOPER12 xltypeNum** または **xltypeErr**)
  
供給された引数リスト、範囲内のセル、配列内の要素に、数字以外の文字が存在する場合の、引数の合計、あるいは #VALUE!。
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

