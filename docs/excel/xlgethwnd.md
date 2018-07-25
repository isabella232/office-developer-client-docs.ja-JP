---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd function [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798995"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ウィンドウの最上位のウィンドウ ハンドルを返します。
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>パラメーター

この関数には引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

**val.w** フィールドにウィンドウ ハンドル (**xltypeInt**) が格納されます。 
  
## <a name="remarks"></a>注釈

この関数は、Windows API のコードを記述するために役立ちます。
  
[Excel4](excel4-excel12.md) または [Excel4v](excel4v-excel12v.md) を使用して、この関数を呼び出すと、返される XLOPER 整数変数は、16 ビット符号付き short int になります。この場合に格納できるのは、32 ビット Windows ハンドルの下位 16 ビットのみです。上位の部分を確認するには、コードですべてのオープン ウィンドウを反復処理し、上位の部分との一致を見つける必要があります。Excel 2007 以降では、**XLOPER12** の整数変数は 32 ビットの符号付き整数になり、すべてのオープン ウィンドウを反復処理する必要がなくなっています。 
  
### <a name="example"></a>例

`SAMPLES\GENERIC\GENERIC.C` で、[fShowDialog 関数](fshowdialog.md) のコードを参照してください。
  
## <a name="see-also"></a>関連項目

- [xlGetInst](xlgetinst.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

