---
title: HOUR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: 日時または式の 1 日の時間を表す 0 から 23 の整数を返します。
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805539"
---
# <a name="hour-function-visioshapesheet"></a>HOUR 関数 (VisioShapeSheet)

_日時_または_式_の 1 日の時間を表す 0 から 23 の整数を返します。
  
## <a name="syntax"></a>構文

時間 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**可変型 (Varies)** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> | 現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
## <a name="remarks"></a>注釈

*Datetime*と*式*の日付コンポーネントが破棄されます。 
  
丸めは行われません。 *Datetime*が存在しないか、有効な結果に変換することはできません、する場合、関数はエラーを返します。 
  
戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。 
  
時間関数では、結果の小数部分が 1 日午前 0 時からの分数を表す*式*の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

HOUR("15:45")
  
15 を返します。
  
## <a name="example-2"></a>例 2

HOUR("May 30, 1997 3:45:24 PM")
  
15 を返します。
  
## <a name="example-3"></a>例 3

HOUR(0.5)
  
12 を返します。
  
## <a name="example-4"></a>例 4

HOUR("5/30/1997")
  
0 を返します。
  

