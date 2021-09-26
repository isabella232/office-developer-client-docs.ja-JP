---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing function [excel 2007],TempMissing12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2ef271941e7ae594bbb0baa88e7a7e197966d2a5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611232"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**xltypeMissing** 型の一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>パラメーター

この関数にパラメーターはありません。
  
## <a name="return-value"></a>戻り値

**xltypeMissing** **XLOPER**/ **XLOPER12** へのポインターを返します。
  
## <a name="example"></a>例

この例では、**TempMissing12** を使用して **xlcWorkspace** の 3 つの欠落した引数を指定し、その後に **ブール値** **FALSE** を続けて、ワークシートのスクロール バーの表示を抑制します。最初の 3 つの引数は、他のワークスペースの設定に対応しますが、それらの設定は影響を受けません。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

