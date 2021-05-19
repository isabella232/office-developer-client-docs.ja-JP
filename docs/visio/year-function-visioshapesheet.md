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
description: システムの現在の地域と言語の設定で設定された短い日付スタイルに従って書式設定された、日付または式のグレゴリオ暦年を表す整数を返します。
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420711"
---
# <a name="year-function-visioshapesheet"></a>YEAR 関数 (VisioShapeSheet)

システムの現在の地域と言語の設定で設定された短い日付スタイルに従って書式設定された、日付または式のグレゴリオ暦年を表す整数を返します。
  
## <a name="syntax"></a>構文

YEAR(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
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
  
数値は四捨五入されません。 datetime  _が見_ つからないか、有効な日付または時刻として解釈できない場合、YEAR はエラーを返します。 
  
YEAR 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表す式の単一の数値も受け入れられます。 
  
## <a name="example-1"></a>例 1

YEAR("10/27/2007 13:45:24")
  
2007 を返します。
  
## <a name="example-2"></a>例 2

YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)
  
2007 を返します。
  
## <a name="example-3"></a>例 3

YEAR(35580.6337)
  
1997 を返します。
  

