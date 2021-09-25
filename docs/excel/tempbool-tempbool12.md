---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- tempbool function [excel 2007],TempBool12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 47c86ac41c49ae1e3de9a5f065294215f95822db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576675"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**ブール値** **TRUE** または **FALSE** を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>パラメーター

 _b_ (**int**)
  
**FALSE** を返すには 0 を使用します。**TRUE** を返すには 0 以外の値を使用します。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

渡された論理値を含む **xltypeBool** **ブール値** を返します。 
  
## <a name="example"></a>例

次の例では、**TempBool12** 関数を使用して、ステータス バーをクリアにします。[Excel/Excel12f](excel-excel12f.md) 関数が呼び出されると、一時メモリが解放されます。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

