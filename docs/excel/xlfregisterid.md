---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid function [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303879"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel から呼び出された DLL コマンドから呼び出すことができます。関数が既に登録されている場合は、その関数を再登録しないで、関数の既存の登録 ID を返します。関数がまだ登録されていない場合は、その関数を登録して、登録 ID を返します。
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>パラメーター

_pxModuleText_ (**xltypeStr**)
  
関数が含まれている DLL の名前。
  
_pxProcedure_ (**xltypeStr** または **xltypeNum**)
  
文字列の場合は、呼び出す関数の名前です。数字の場合は、呼び出す関数のエクスポートの順序番号です。明確で堅牢にするために、常に文字列形式を使用します。
  
_pxTypeText_ (**xltypeStr**)
  
関数へのすべての引数の型と関数の戻り値の型を指定する、省略可能な文字列。詳しくは、「解説」セクションを参照してください。**xlAutoRegister** を定義するスタンドアロン DLL (XLL) では、この引数を省略できます。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

後続の **xlfUnregister** への呼び出しに使用できる、関数 (**xltypeNum**) の登録 ID を返します。
  
## <a name="remarks"></a>注釈

登録 ID は後で登録解除する際に必要になるが、維持のために気を使いたくない、という場合に、この関数が役立ちます。また、割り当てる関数が DLL にある場合は、メニュー、ツール、およびボタンへの割り当てにも役立ちます。
  
**xlfRegister** に指定された有効な _pxFunctionText_ 引数を使用して DLL または XLL 関数が登録されている場合は、関数 **xlfEvaluate** に _pxFunctionText_ を渡すことで、その登録 ID を取得することもできます。
  
## <a name="see-also"></a>関連項目

- [REGISTER](xlfregister-form-1.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

