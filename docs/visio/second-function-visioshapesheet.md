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
description: datetime または expression の秒の部分を表す 0 ~ 59 の整数を返します。
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404877"
---
# <a name="second-function-visioshapesheet"></a>SECOND 関数 (VisioShapeSheet)

_datetime_または_expression_の秒の部分を表す 0 ~ 59 の整数を返します。
  
## <a name="syntax"></a>構文

2番目 ("* * *datetime* * *" |* **式** * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> |非現地_日付_を評価するときに使用するロケール識別子を指定します。 ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

_datetime_または_expression_の日付コンポーネントは破棄されます。 
  
数値は四捨五入されません。 _datetime_が指定されていない場合、または有効な結果に変換できない場合、この関数はエラーを返します。 
  
2番目の関数では、 _expression_に単一の数値を使用することもできます。この場合、小数点の部分が午前0時からの1日の小数部分を表します。 
  
## <a name="example-1"></a>例 1

2番目 ("05/30/1997 13:45:32")
  
32 を返します。
  
## <a name="example-2"></a>例 2

SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)
  
52 を返します。
  
## <a name="example-3"></a>例 3

2番目 (0.6337)
  
32 を返します。
  

