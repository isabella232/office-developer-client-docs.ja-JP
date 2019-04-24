---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- func1 function [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304082"
---
# <a name="func1"></a>Func1

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザー定義のワークシート関数の例で、返される静的な文字列値について説明します。GENERIC.xll が読み込まれると、GENERIC.xll によってこの関数が登録されて、ワークシートから呼び出すことができるようになります。
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>パラメーター

 _px_ (**LPXLOPER**)
  
この引数は無視され、Microsoft Excel をトリガーして関数を呼び出すためだけの役目を果たします。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 **LPXLOPER12**: 常に文字列 "Func1"
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

