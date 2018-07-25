---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- tempnum12 function [excel 2007],TempNum function [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798949"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ワークシートの番号を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数 (IEEE 8 バイトの倍精度浮動小数点型)。 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>パラメーター

 _d_ (**double**)
  
対象の値。IEEE 規格の非正規数は現在サポートされていないため、ゼロに丸められます。負の無限大に対応しています。
  
## <a name="return-value"></a>戻り値

渡される値を含む数値型 **xltypeNum** を返します。渡された値が非正規数の場合はゼロを返します。 
  
## <a name="example"></a>例

この例では、**TempNum12** 関数を使用して、**xlfGetWorkspace** に引数を渡しています。
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

