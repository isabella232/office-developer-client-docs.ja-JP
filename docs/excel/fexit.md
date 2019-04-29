---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit function [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429916"
---
# <a name="fexit"></a>fExit

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
GENERIC.xll をアンロードするサンプル ユーザー定義コマンド。GENERIC.xll が読み込まれると、このコマンドにアクセスするのに使用するユーザー定義メニュー [Generic] を作成します。 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>パラメーター

この関数にはパラメーターはありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は、常に 1 を返します。
  
## <a name="remarks"></a>注釈

これは、GENERIC.xll を終了するためにユーザーが開始するルーチンです。この関数で単に `UNREGISTER("GENERIC.XLL")` を呼び出すことは避けてください。その場合、この DLL 内のすべての関数が強制的に登録解除されます。これらの関数が他のいずれかに登録されている場合も同じです。代わりに、一度に 1 つずつ関数を登録解除してください。 
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

