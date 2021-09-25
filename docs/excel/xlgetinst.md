---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst function [excel 2007]
ms.localizationpriority: medium
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1346eb97fb70912c5acfb49bebffa016e05a17ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572341"
---
# <a name="xlgetinst"></a>xlGetInst

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
現在 DLL を呼び出している Microsoft Excel インスタンスのインスタンス ハンドルを返します。
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>パラメーター

この関数には引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

インスタンス ハンドル (**xltypeInt**) は、**val.w** フィールドに取り込まれます。 
  
## <a name="remarks"></a>注釈

この関数を使用すると、DLL を呼び出している Excel の複数の実行中インスタンスを特定できます。
  
[Excel4](excel4-excel12.md) または [Excel4v](excel4v-excel12v.md) を使用してこの関数を呼び出すと、返される XLOPER 整数変数は、16 ビット符号付き short int になります。この場合に格納できるのは、32 ビット Windows ハンドルの下位 16 ビットのみです。Excel 2007 以降では、**XLOPER12** の整数変数は 32 ビットの符号付き整数になり、すべてのオープン ウィンドウを反復処理する必要がなくなっています。 
  
> [!IMPORTANT]
> **xlGetInst** 関数を 64 ビット版の Microsoft Excel で使用すると、失敗します。これは、**xltypeInt** 値の型の大きさが、Excel によって返される 64 ビット長のハンドルを保持できないためです。このため、Excel 2010 では [xlGetInstPtr](xlgetinstptr.md) という名前の新しい関数が導入されました。この関数は、32 ビットと 64 ビットのどちらのバージョンの Excel でも正常に動作します。 
  
## <a name="example"></a>例

次の例では、呼び出し元 Excel の最終コピーのインスタンスを、呼び出し元 Excel の現在のコピーと比較します。この 2 つが同じであれば 1 を返し、そうでなければ 0 を返します。関数が失敗した場合は、-1 を返します。
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>関連項目



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

