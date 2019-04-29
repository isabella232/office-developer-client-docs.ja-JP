---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- convertxlreftoxlref12 function [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432031"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**XLREF** を **XLREF12** に変換しようとする Framework 関数。
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>パラメーター

 _pxRef_ (**LPXLREF**)
  
ソースの参照構造体へのポインター。
  
 _pxRef12_ (**LPXLREF12**)
  
変換した値が配置されるターゲットの参照構造体へのポインター。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 変換が成功した場合は **TRUE**。それ以外の場合は **FALSE**。 
  
## <a name="remarks"></a>注釈

渡された **XLREF** が有効な場合、この操作は常に成功します。それとは対照的に、[ConvertXLRef12ToXLRef](convertxlref12toxlref.md) で実行する **XLREF12** から **XLREF** への逆の変換では、指定された参照が、前のバージョンでサポートされていない Excel 2007 ワークシートの一部を参照している場合、変換操作は失敗します。
  
## <a name="example"></a>例

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

