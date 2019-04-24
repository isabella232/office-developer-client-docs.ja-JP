---
title: YEAR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: datetime または expression のグレゴリオ暦の年を表す整数を返します。これは、システムの現在の地域と言語の設定によって設定された短い日付形式に従って書式設定されます。
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351654"
---
# <a name="year-function-visioshapesheet"></a>YEAR 関数 (VisioShapeSheet)

_datetime_または_expression_のグレゴリオ暦の年を表す整数を返します。これは、システムの現在の地域と言語の設定によって設定された短い日付形式に従って書式設定されます。
  
## <a name="syntax"></a>構文

YEAR ("* * *datetime* * *" |* **式** * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**さまざま** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。 ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>解説

_datetime_または_expression_の時刻コンポーネントは破棄されます。 
  
数値は四捨五入されません。 _datetime_が指定されていない場合、または有効な日付または時刻として解釈できない場合、YEAR はエラーを返します。 
  
YEAR 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。 
  
## <a name="example-1"></a>例 1

YEAR ("10/27/2007 13:45:24")
  
2007 を返します。
  
## <a name="example-2"></a>例 2

YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)
  
2007 を返します。
  
## <a name="example-3"></a>例 3

年 (35580.6337)
  
1997 を返します。
  

