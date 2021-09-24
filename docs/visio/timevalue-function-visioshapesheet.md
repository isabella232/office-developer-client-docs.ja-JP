---
title: TIMEVALUE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
ms.localizationpriority: medium
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: システムの地域と言語の設定に基づいて、datetime または式で表される時刻値を返します。
ms.openlocfilehash: 19b6d92fa5efeb1f9881e429a3368b20b3bc9893
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549470"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE 関数 (VisioShapeSheet)

システムの地域と言語の設定に基づいて、datetime または式で表される時刻値を返します。  
  
## <a name="syntax"></a>構文

TIMEVALUE(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須かどうか  <br/> |**さまざま** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |オプション  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
## <a name="remarks"></a>注釈

datetime または _式の日付__コンポーネントは_ 破棄されます。 
  
datetime  _が見_ つからない場合、または有効な結果に変換できない場合、この関数は値を返#VALUE! エラーを返します。 
  
TIMEVALUE 関数は、結果の 10進部分が午前 0 時からの 1 日の小数部を表す式の単一の数値も受け入れられます。 
  
## <a name="example-1"></a>例 1

TIMEVALUE("6:00 AM")
  
6:00 AM を表す値を返します。
  
## <a name="example-2"></a>例 2

TIMEVALUE("14:30")+4 eh.+30 em.
  
19:00:00 を表す値を返します。
  
## <a name="example-3"></a>例 3

TIMEVALUE("11 AM, July 1, 1997")
  
11:00 AM を表す値を返します。
  
## <a name="example-4"></a>例 4

TIMEVALUE(0.6337)
  
15:12:32 を表す値を返します。
  
## <a name="example-5"></a>例 5

TIMEVALUE("7:89")
  
#VALUE! エラーを返します。
  

