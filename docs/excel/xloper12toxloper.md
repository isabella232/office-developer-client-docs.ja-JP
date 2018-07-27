---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper function [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798993"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
新しい **XLOPER12** から古いい **XLOPER** への変換に使用する変換ルーチンです。
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>パラメーター

_pxloper12_ (**LPXLOPER12**)
  
変換対象のソース **XLOPER12** へのポインター。 
  
_pxloper_ (**LPXLOPER**)
  
変換された値を格納するターゲット **XLOPER** へのポインター。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

変換が成功した場合は **TRUE**。それ以外の場合は **FALSE**。 
  
## <a name="remarks"></a>注釈

**XLOPER12** の型によっては、この関数は、変換されてターゲット **XLOPER** をポイントする値に新しいメモリ バッファーを割り当てます。変換が成功した場合、そのコピーに関連付けられたメモリを解放する責任は、呼び出し元にあります。メモリを解放するには、**FreeXLOperT** を使用するか、**free** を使用して直接解放します。
  
変換が失敗した場合は、呼び出し元でメモリを解放する必要はありません。
  
**XLOPER12** から **XLOPER** への変換は、**XLOPER12** に収まりきらないほど大きい配列や参照、または長い文字列が **XLOPER** に格納されていると、失敗することがあります。 
  
**XLOPER12** の Unicode ワイド文字文字列は、ロケールに依存する方法で **XLOPER** の ASCII バイト文字列に変換されます。 
  
**XLOPER12** **xltypeInt** は 32 ビット符号付き整数です。**XLOPER** **xltypeInt** は 16 ビット符号付き整数です。指定された **XLOPER12** 整数が **XLOPER** 整数の制限を超える場合は、その整数は 8 バイトの double に変換され、**xltypeNum** 型の **XLOPER** で返されます。この場合にのみ、この関数は変換した **XLOPER** の型を変更します。
  
### <a name="example"></a>例

この関数のコードについては、`\SAMPLES\FRAMEWRK\FRAMEWRK.C` ファイルを参照してください。 
  
## <a name="see-also"></a>関連項目

- [フレームワーク ライブラリの関数](functions-in-the-framework-library.md)

