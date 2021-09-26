---
title: xlfRegister (形式 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister function [excel 2007]
ms.localizationpriority: medium
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6268339f9dddff6d61ec843bb7d498fc0710d38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611169"
---
# <a name="xlfregister-form-2"></a>xlfRegister (形式 2)

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel から呼び出された DLL コマンドまたは XLL コマンドから呼び出すことができます。これは、Excel XLM マクロ シートからの **REGISTER** の呼び出しと同等です。 
  
**xlfRegister** 関数は、次の 2 つの形式で呼び出すことができます。 
  
- [xlfRegister (形式 1)](xlfregister-form-1.md): コマンドや関数を個々に登録します。
    
- xlfRegister (形式 2): XLL を読み込んでアクティブ化します。
    
この関数を形式 2 で呼び出した場合は、[xlAutoOpen](xlautoopen.md) プロシージャを含む XLL の読み込みとアクティブ化のみ行います。 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>パラメーター

 _pxModuleText_ (**xltypeStr**)
  
読み込みとアクティブ化を行う DLL 名。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功すると、DLL 名 (**xltypeStr**) を返します。それ以外の場合は、#VALUE! エラーを返します。
  
## <a name="see-also"></a>関連項目



[重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

