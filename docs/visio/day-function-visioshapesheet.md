---
title: DAY 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: datetime または expression の日を表す 1 ~ 31 の整数を返します。 DAY 関数ではグレゴリオ暦が使用されます。
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360298"
---
# <a name="day-function-visioshapesheet"></a>DAY 関数 (VisioShapeSheet)

_datetime_または_expression_の日を表す 1 ~ 31 の整数を返します。 DAY 関数ではグレゴリオ暦が使用されます。
  
## <a name="syntax"></a>構文

DAY ("* * *datetime* * *" |* **式** * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>解説

_datetime_または_expression_の時刻コンポーネントは破棄されます。 
  
数値は四捨五入されません。 _datetime_が指定されていない場合、または有効な結果に変換できない場合、関数はエラーを返します。 
  
DAY 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。 
  
## <a name="example-1"></a>例 1

DAY("May 30, 1997 15:45:24")
  
30 を返します。
  
## <a name="example-2"></a>例 2

DAY(DATEVALUE("May 30, 1997")+7 ed.)
  
6 を返します。
  
## <a name="example-3"></a>例 3

日 (35580.6337)
  
30 を返します。
  

