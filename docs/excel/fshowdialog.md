---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog function [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798889"
---
# <a name="fshowdialog"></a>fShowDialog

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ネイティブ Windows ダイアログ ボックスの例を読み込んで表示するユーザー定義コマンドの例です。GENERIC.xll が読み込まれるとき、このコマンドにアクセスするユーザー定義メニュー [Generic] を作成します。
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>パラメーター

この関数にはパラメーターはありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は、正常に完了したことを示す整数値 0 を返します。
  
## <a name="remarks"></a>注釈

ネイティブ Windows ダイアログ ボックスを表示する手順は次のとおりです。
  
1. **GetHwnd** を使用して、Microsoft Excel メイン ウィンドウ ハンドルを取得します。
    
2. **HookExcelWindow** を使用して Excel メイン ウィンドウをフックします。
    
3. **DialogBox** を使用してダイアログ ボックスを表示します。
    
4. **UnhookExcelWindow** を使用して Excel メイン ウィンドウのフックを解除します。
    
### <a name="example"></a>例

この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[汎用 DLL の関数](functions-in-the-generic-dll.md)

