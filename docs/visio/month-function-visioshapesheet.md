---
title: MONTH 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: 1 から 12 月を表す整数を返します。
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805908"
---
# <a name="month-function-visioshapesheet"></a>MONTH 関数 (VisioShapeSheet)

1 から 12 月を表す整数を返します。
  
## <a name="syntax"></a>構文

月 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>�߂�l

整数型 (Integer)
  
## <a name="remarks"></a>Remarks

_日時_または_式_の時間の構成要素は破棄されます。 
  
数値は四捨五入されません。入力文字列が指定されていない場合、または有効な結果に変換できない場合、MONTH 関数はエラーを返します。
  
戻り値は、システムの現在の [地域別設定] に設定されている短い形式の日付で書式設定されます。
  
MONTH 関数では、結果の整数部分が、1899 年 12 月 30 日以降の日数を表す_式_の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

MONTH("May 30, 1999 13:45:24")
  
5 を返します。
  
## <a name="example-2"></a>例 2

MONTH(DATEVALUE("May 30, 1999")+7 ed.)
  
6 を返します。
  
## <a name="example-3"></a>例 3

MONTH(35580.6337)
  
5 を返します。
  

