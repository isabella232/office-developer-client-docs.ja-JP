---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- convertxlref12toxlref function [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 826428edb57eba9e17d601164aa8b4b797fc8929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798770"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**XLREF12** から **XLREF** への変換を試みます。
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>パラメーター

 _pxRef12_ (**LPXLREF12**)
  
ソースの参照構造体へのポインター。
  
 _pxRef_ (**LPXLREF**)
  
変換した値が配置されるターゲットの参照構造体へのポインター。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 変換が成功した場合は **TRUE**。それ以外の場合は **FALSE**。 
  
## <a name="remarks"></a>注釈

指定した参照が以前のバージョンではサポートされていない Excel 2007 ワークシートの部分を参照している場合、**XLREF12** から **XLREF** への変換は失敗します。 
  
## <a name="example"></a>例

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a>関連項目



[フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

