---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fdialog function [excel 2007],fDialog12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: afcf924e04f833ff823647eef603824652347e5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568195"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザー定義コマンドの例で、C API のダイアログ ボックスの機能を使用して、DLL 内で Microsoft Excel UDD (ユーザー定義のダイアログ ボックス) を作成する方法を説明します。GENERIC.xll が読み込まれると、このコマンドにアクセスするのに使用するユーザー定義メニュー [Generic] を作成します。
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>パラメーター

この関数にはパラメーターはありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は、常に 1 を返します。
  
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

