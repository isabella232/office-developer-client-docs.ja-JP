---
title: DATEVALUE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: datetime または expression で表される日付の値を返します。
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360313"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE 関数 (VisioShapeSheet)

_datetime_または_expression_で表される日付の値を返します。
  
## <a name="syntax"></a>構文

DATEVALUE ("* * *datetime* * *" |* **式** * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

Datetime
  
## <a name="remarks"></a>解説

*datetime*または*expression*の時刻コンポーネントは破棄されます。 
  
*datetime*が指定されていない場合、または有効な結果に変換できない場合は、DATEVALUE は #VALUE を返します。 エラーを返します。 
  
戻り値は、システムの現在の [地域の設定] に設定されている短い形式の日付で表示されます。 
  
また、DATEVALUE 関数では、 *expression*に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。 
  
## <a name="example-1"></a>例 1

DATEVALUE(NOW( ))+5 ed.
  
現在から 5 日後の日付を返します。
  
## <a name="example-2"></a>例 2

DATEVALUE ("7/19/1995 12:30")
  
日付を返します。
  
## <a name="example-3"></a>例 3

DATEVALUE("May 33, 1997")
  
#VALUE! エラーを返します。
  
## <a name="example-4"></a>例 4

DATEVALUE (35580.6337)
  
5/30/1997 を返します。
  

