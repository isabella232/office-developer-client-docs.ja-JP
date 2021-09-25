---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- funcfib function [excel 2007]
ms.localizationpriority: medium
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4f1fceedaf7e152fbbfd5e708d9da55e161f43ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552221"
---
# <a name="funcfib"></a>FuncFib

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
N 番目のフィボナッチ数を計算するユーザー定義ワークシート関数の例です。GENERIC.xll が読み込まれるときに、ワークシートから呼び出すことができるように、この関数を登録します。
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>パラメーター

 _pxN_ (**LPXLOPER12**)
  
N 番目のフィボナッチ数が必要とされる N の値。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

(成功した場合は **xltypeNum LPXLOPER12**、それ以外の場合は **xltypeErr**) 
  
N 番目のフィボナッチ数。
  
## <a name="remarks"></a>注釈

この関数は、関数ブロック内で戻り値 **XLOPER12** として定義された静的変数を使用します。これはスレッド セーフではないため、この関数もスレッド セーフではありません。Excel 2007 以降では、この戦略を使用して **XLOPER** または **XLOPER12** を返すワークシート関数をスレッド セーフとして登録しないでください。
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

