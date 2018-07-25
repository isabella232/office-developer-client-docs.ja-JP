---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798994"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
現在 DLL を呼び出している Microsoft Excel インスタンスのインスタンス ハンドルを返します。
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>パラメーター

この関数には引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

インスタンス ハンドル (**xltypeBigData**) は **val.bigdata.h.hdata** フィールドに格納されます。 
  
## <a name="remarks"></a>注釈

この関数を使用すると、DLL を呼び出している Excel の複数の実行中インスタンスを特定できます。
  
この関数は、32 ビットと 64 ビットの両方のバージョンの Excel で適切な値を返します。 [xlGetInst](xlgetinst.md) 関数の拡張機能として Excel 2010 で導入され、32 ビット バージョンの Excel でのみ正常に動作します。 
  
この関数は、API のコールバック関数の [Excel4 と Excel12](excel4-excel12.md) の両方を使用して呼び出されたときに正常に作動します。これは **XLOPER** と **XLOPER12** が **xltypeBigData** の型の値をサポートする同じ構造を持つからです。 
  
## <a name="example"></a>例

次の例では、呼び出し元 Excel の最終コピーのインスタンスを、呼び出し元 Excel の現在のコピーと比較します。この 2 つが同じであれば 1 を返し、そうでなければ 0 を返します。関数が失敗した場合は、-1 を返します。この例は、Excel の 32 ビット バージョンと 64 ビット バージョンの両方で機能します。
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
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

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

