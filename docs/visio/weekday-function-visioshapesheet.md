---
title: WEEKDAY 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: 日付または式の曜日を表す 1 ~ 7 の整数を返します。
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404807"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY 関数 (VisioShapeSheet)

日付または式の平日を表す 1 ~ 7  _の整数を_ 返  _します_。
  
## <a name="syntax"></a>構文

WEEKDAY(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**さまざま** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

datetime または _式の時刻__コンポーネントは_ 破棄されます。 
  
結果は月曜日 (1) から日曜日 (7) に対応します。 数値は四捨五入されません。 datetime  _が見_ つからないか、有効な日付または時刻として解釈できない場合、関数は日付を返#VALUE! エラーを返します。 
  
また、WEEKDAY 関数は、結果の整数部分が 1899 年 12 月 30 日からの日数を表す式の単一の数値を受け入れられます。 
  
## <a name="example-1"></a>例 1

WEEKDAY("May 30, 1999")
  
7 を返します。
  
## <a name="example-2"></a>例 2

WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)
  
2 を返します。
  
## <a name="example-3"></a>例 3

WEEKDAY(35880.6337)
  
4 を返します。
  

