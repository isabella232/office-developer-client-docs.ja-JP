---
title: SECOND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
ms.localizationpriority: medium
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: datetime または式の秒のコンポーネントを表す 0 ~ 59 の整数を返します。
ms.openlocfilehash: f9f8a3f823ed4b0989abd6f338aaf44a0f56a059
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553928"
---
# <a name="second-function-visioshapesheet"></a>SECOND 関数 (VisioShapeSheet)

datetime または式の seconds コンポーネントを表す 0 ~ 59 の  _整数を_ 返  _します_。
  
## <a name="syntax"></a>構文

SECOND(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |オプション  <br/> |**数値型 (Numeric)** <br/> |非地域的な日時の評価に使用するロケール  _識別子_ です。 ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

datetime または _式の日付__コンポーネントは_ 破棄されます。 
  
数値は四捨五入されません。 datetime  _が見_ つからないか、有効な結果に変換できない場合、この関数はエラーを返します。 
  
SECOND 関数は、結果の 10進部分が午前 0 時からの 1 日の端数を表す式の単一の数値も受け入れられます。 
  
## <a name="example-1"></a>例 1

SECOND("05/30/1997 13:45:32")
  
32 を返します。
  
## <a name="example-2"></a>例 2

SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)
  
52 を返します。
  
## <a name="example-3"></a>例 3

SECOND(0.6337)
  
32 を返します。
  

