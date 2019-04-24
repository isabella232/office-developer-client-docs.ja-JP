---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- xlstack function [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310158"
---
# <a name="xlstack"></a>xlStack

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
スタック上の空き領域を確認します。
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>パラメーター

この関数に引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

スタック上に残っているバイト数 (**xltypeInt**) を返します。
  
## <a name="remarks"></a>注釈

最近のバージョンの使用可能なスタック領域の容量は、**XLOPER** の 16 ビットの符号付き整数に収まりません。つまり、**xlStack** は **XLOPER** および **Excel4** または **Excel4v** を使用して呼び出したときに -32767 から 32768 の間の値を返すことができる、ということです。この場合に正しい値を取得するには、戻り値を unsigned short 型にキャストします。
  
Excel 2007 以降では、**XLOPER12** および **Excel12** または **Excel12v** を使用して、この関数を呼び出す必要があります。その場合、戻り値は使用可能なスタック領域の容量か、64 KB のいずれか小さい方になります。
  
Excel では、スタック上の空き領域に制限があります。この容量を超えないように注意する必要があります。非常に大きなデータ構造を配置したり、可能な限り多くのローカル変数を静的にしてはいけません。関数を再帰的に呼び出さないようにしてください。これを行うと、スタックがすぐにいっぱいになります。
  
スタックをオーバーランしている疑いがある場合は、この関数を頻繁に呼び出して、スタック領域がどの程度残っているか確認します。
  
## <a name="example"></a>例

最初の例では、スタックの空き領域の容量が示された警告メッセージが表示されます。これは `\SAMPLES\EXAMPLE\EXAMPLE.C` に格納されています。2 番目の例も同じことをします (**XLOPER** を使用)。これは SDK のコード例には含まれていません。
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a>関連項目

- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

