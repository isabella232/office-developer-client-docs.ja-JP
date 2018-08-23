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
description: 日時または式で表される日付の値を返します。
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805183"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE 関数 (VisioShapeSheet)

_日時_または_式_で表される日付の値を返します。
  
## <a name="syntax"></a>構文

DATEVALUE ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

日付/時刻
  
## <a name="remarks"></a>注釈

*日時*または*式*で任意の時間コンポーネントを破棄します。 
  
*Datetime*が存在しないか、有効な結果に変換することはできませんである場合、datevalue 関数は、#VALUE を返します。 エラーを返します。 
  
戻り値は、システムの現在の [地域の設定] に設定されている短い形式の日付で表示されます。 
  
DATEVALUE 関数は、結果の整数部分が、1899 年 12 月 30 日以降の日付を表す*式*の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

DATEVALUE(NOW( ))+5 ed.
  
現在から 5 日後の日付を返します。
  
## <a name="example-2"></a>例 2

DATEVALUE("7/19/1995 12:30")
  
日付を返します。
  
## <a name="example-3"></a>例 3

DATEVALUE("May 33, 1997")
  
#VALUE! エラーを返します。
  
## <a name="example-4"></a>例 4

DATEVALUE(35580.6337)
  
5/30/1997 を返します。
  

