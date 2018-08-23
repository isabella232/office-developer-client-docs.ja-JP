---
title: MINUTE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: 0 から 59 日時または式の分コンポーネントを表す整数を返します。
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805905"
---
# <a name="minute-function-visioshapesheet"></a>MINUTE 関数 (VisioShapeSheet)

0 から 59*日時*または*式*の分コンポーネントを表す整数を返します。 
  
## <a name="syntax"></a>構文

分 (" *datetime* "| *式* [、 *lcid* ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

_Datetime_と_式_の日付コンポーネントが破棄されます。 
  
丸めは行われません。 _Datetime_が存在しないか、有効な結果に変換することはできません、する場合、関数はエラーを返します。 
  
戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。
  
MINUTE 関数では、小数部分が 1 日午前 0 時からの分数を表す_式_の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

MINUTE("7/7/1999 13:45:24")
  
45 を返します。
  
## <a name="example-2"></a>例 2

MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)
  
13 を返します。
  
## <a name="example-3"></a>例 3

MINUTE(0.575)
  
48 を返します。
  

