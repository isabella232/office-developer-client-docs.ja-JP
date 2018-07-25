---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12 function [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799008"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
古い **XLOPER** から新しい **XLOPER12** への変換に使用する変換ルーチン。
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>パラメーター

_pxloper_ (**LPXLOPER**)
  
変換対象のソース **XLOPER** へのポインター。 
  
_pxloper12_ (**LPXLOPER12**)
  
変換された値を格納するターゲット **XLOPER12** へのポインター。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

変換が成功した場合は **TRUE**。それ以外の場合は **FALSE**。 
  
## <a name="remarks"></a>注釈

**XLOPER** の型によっては、この関数は、変換されてターゲット **XLOPER12** をポイントする値に新しいメモリ バッファーを割り当てます。変換が成功した場合、そのコピーに関連付けられたメモリを解放する責任は、呼び出し元にあります。メモリを解放するには、**FreeXLOper12T** を使用するか、**free** を使用して直接解放します。
  
変換が失敗した場合は、呼び出し元でメモリを解放する必要はありません。
  
通常は、任意の **XLOPER** を **XLOPER12** に変換できます。それとは対照的に、**XLOPER12** を **XLOPER** に変換する場合、**XLOPER** に格納するには大きすぎる配列または参照が **XLOPER12** に含まれていると、変換は失敗します。 
  
**XLOPER** ASCII バイト文字列は、ロケールに依存する方法で **XLOPER12** Unicode 再度文字列に変換されます。 
  
### <a name="example"></a>例

この関数のコードについては、`\SAMPLES\FRAMEWRK\FRAMEWRK.C` ファイルを参照してください。 
  

