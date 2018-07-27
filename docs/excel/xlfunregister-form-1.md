---
title: xlfUnregister (形式 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister function [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798981"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (形式 1)

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel から呼び出された DLL コマンドまたは XLL コマンドから呼び出すことができます。これは、**UNREGISTER** を Excel XLM マクロ シートから呼び出すのと同等です。 
  
**xlfUnregister** 関数は、次の 2 つの形式で呼び出すことができます。 
  
- 形式 1: 個々のコマンドや関数の登録を解除します。
    
- 形式 2: XLL のアンロードと非アクティブ化を行います。
    
形式 1 で呼び出されると、この関数は、**xlfRegister** または **REGISTER** を使用して既に登録されている DLL 関数またはコマンドの使用カウントを減らします。既に使用カウントが 0 の場合、この関数の効果はありません。DLL 内のすべての関数の使用カウントが 0 になると、DLL はメモリからアンロードされます。
  
**xlfRegister** (形式 1) は、関数またはコマンドの登録 ID ともみなされる非表示名 (関数のテキスト引数 _pxFunctionText_) も定義します。関数の登録を解除する場合は、関数ウィザードにその関数の名前が表示されなくなるように、**xlfSetName** を使用してこの名前を削除する必要があります。詳しくは、「[Excel アドイン (XLL) 開発における既知の問題](known-issues-in-excel-xll-development.md)」を参照してください。
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>パラメーター

_pxRegisterId_ (**xltypeNum**)
  
登録を解除する関数の登録 ID。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合は **TRUE** (**xltypeBool**) を返します。それ以外の場合は FALSE を返します。
  
## <a name="remarks"></a>注釈

関数の登録 ID は、関数の最初の登録時に **xlfRegister** によって返されます。また、[xlfRegisterId 関数](xlfregisterid.md) または [xlfEvaluate 関数](xlfevaluate.md)を呼び出して取得することもできます。関数がまだ登録されていない場合は、xlfRegisterId はその関数を登録しようとすることにご注意ください。このため、単に関数の登録を解除する目的で ID を取得しようとしているのであれば、登録された名前を **xlfEvaluate** に渡して ID を取得することをお勧めします。関数が登録されていない場合、**xlfEvaluate** は #NAME? エラーで失敗します。 
  
## <a name="example"></a>例

`\SAMPLES\GENERIC\GENERIC.C` の **fExit** 関数のコードを参照してください。
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a>関連項目

- [xlfRegister (形式 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (形式 2)](xlfunregister-form-2.md)
- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

