---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf function [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424799"
---
# <a name="debugprintf"></a>debugPrintf

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
null で終わるバイト文字列を、Windows SDK 関数 **OutputDebugStringA** を使用してアクティブなデバッガーに書き込むフレームワーク ライブラリ関数。アプリケーションにデバッガーがない場合は、システムのデバッガーに文字列が表示されます。アプリケーションにデバッガーがなく、システムのデバッガーがアクティブでない場合、**debugPrintf** は何の動作も行いません。 
  
この関数は値を返しません。
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>パラメーター

 _lpFormat (LPSTR)_
  
形式文字列。**sprintf** 関数とともに用いられる文字列の構文とルールに従います。 
  
 _arguments_
  
形式文字列に一致する 0 個以上の引数。
  
## <a name="example"></a>例

この関数は、関数にコントロールが渡されたことを示す文字列を印刷します。コンパイルする前に _DEBUG フラグを定義する必要があります。未定義のままでは、この関数は何の動作も行いません。
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

