---
title: SECOND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: 0 ~ 59、日時または式の秒の部分を表す整数を返します。
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806354"
---
# <a name="second-function-visioshapesheet"></a>SECOND 関数 (VisioShapeSheet)

0 ~ 59、_日時_または_式_の秒の部分を表す整数を返します。
  
## <a name="syntax"></a>構文

2 つ目 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |現地以外の_datetime_を計算するときに使用されるロケールの識別子です。 ロケール識別子は、システムのヘッダー ファイルに記載されている番号です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

_日時_または_式_の日付コンポーネントが破棄されます。 
  
丸めは行われません。 _Datetime_が存在しないか、有効な結果に変換することはできません、する場合、この関数はエラーを返します。 
  
2 番目の関数は、結果の小数部分が 1 日午前 0 時からの分数を表す_式_の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

SECOND("05/30/1997 13:45:32")
  
32 を返します。
  
## <a name="example-2"></a>例 2

SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)
  
52 を返します。
  
## <a name="example-3"></a>例 3

SECOND(0.6337)
  
32 を返します。
  

