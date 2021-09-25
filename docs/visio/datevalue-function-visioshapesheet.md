---
title: DATEVALUE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
ms.localizationpriority: medium
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: datetime または式で表される日付値を返します。
ms.openlocfilehash: 571d0f319ccbbefa412e2b31bbc01d49ee9ec46c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582814"
---
# <a name="datevalue-function-visioshapesheet"></a>DATEVALUE 関数 (VisioShapeSheet)

datetime または式で表される日付  _値を_ 返  _します_。
  
## <a name="syntax"></a>構文

DATEVALUE(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |オプション  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

Datetime
  
## <a name="remarks"></a>注釈

datetime または  *式内の*  任意の  *時刻コンポーネント*  は破棄されます。 
  
datetime  *が見*  つからないか、有効な結果に変換できない場合、DATEVALUE は値を返#VALUE! エラーを返します。 
  
戻り値は、システムの現在の [地域の設定] に設定されている短い形式の日付で表示されます。 
  
DATEVALUE 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表す式の 1 つの数値値も受け入れられます。 
  
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
  

