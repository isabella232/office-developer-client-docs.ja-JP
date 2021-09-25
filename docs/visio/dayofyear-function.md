---
title: DAYOFYEAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
ms.localizationpriority: medium
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: 1 ~ 366 の整数を返します。日付または式の年の連続日を表します。 DAYOFYEAR 関数はグレゴリオ暦を使用します。
ms.openlocfilehash: 8a73d4c8c7df501e1969d8aa9279f720407d2e7b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559970"
---
# <a name="dayofyear-function"></a>DAYOFYEAR 関数

datetime または式の年の連続日を表す 1 ~ 366 の  _整数を_ 返  _します_。 DAYOFYEAR 関数はグレゴリオ暦を使用します。
  
## <a name="syntax"></a>構文

DAYOFYEAR(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |オプション  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

datetime または  _式内の_ 任意の  _時刻コンポーネント_ は破棄されます。 
  
結果は 1 月 1 日～ 12 月 31 日に対応します。 数値は四捨五入されません。 datetime  _が見_ つからないか、有効な日付または時刻として解釈できない場合、関数はエラーを返します。 
  
DAYOFYEAR 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表す式の単一の数値も受け入れられます。 
  
## <a name="example-1"></a>例 1

DAYOFYEAR("May 30, 1997 13:45:24")
  
150 を返します。
  
## <a name="example-2"></a>例 2

DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)
  
157 を返します。
  
## <a name="example-3"></a>例 3

DAYOFYEAR(35580.6337)
  
150 を返します。
  

