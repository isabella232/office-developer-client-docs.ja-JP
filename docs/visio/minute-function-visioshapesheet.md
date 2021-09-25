---
title: MINUTE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
ms.localizationpriority: medium
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: datetime または式の分のコンポーネントを表す 0 ~ 59 の整数を返します。
ms.openlocfilehash: b57eae5388969461056e6d2fe00b5e1035e8a24b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594518"
---
# <a name="minute-function-visioshapesheet"></a>MINUTE 関数 (VisioShapeSheet)

datetime または式の分のコンポーネントを表す 0 ~ 59 の  *整数を*  返  *します*  。 
  
## <a name="syntax"></a>構文

MINUTE(" *datetime*  "|  *式*  [,  *lcid*  ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |オプション  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

datetime および _式の日付__コンポーネントは_ 破棄されます。 
  
数値は四捨五入されません。 datetime  _が見_ つからないか、有効な結果に変換できない場合、関数はエラーを返します。 
  
戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。
  
MINUTE 関数は、10 進数の部分が午前 0 時からの 1 日の端数を表す式の単一の数値も受け取る。 
  
## <a name="example-1"></a>例 1

MINUTE("7/7/1999 13:45:24")
  
45 を返します。
  
## <a name="example-2"></a>例 2

MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)
  
13 を返します。
  
## <a name="example-3"></a>例 3

MINUTE(0.575)
  
48 を返します。
  

