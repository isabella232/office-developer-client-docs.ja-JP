---
title: MONTH 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
ms.localizationpriority: medium
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: 月を表す 1 ~ 12 の整数を返します。
ms.openlocfilehash: 44e033ab2719a45b6ddfba48ac53b4a4e9606d3b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573888"
---
# <a name="month-function-visioshapesheet"></a>MONTH 関数 (VisioShapeSheet)

月を表す 1 ~ 12 の整数を返します。
  
## <a name="syntax"></a>構文

MONTH(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |オプション  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

datetime または _式の時刻__コンポーネントは_ 破棄されます。 
  
数値は四捨五入されません。入力文字列が指定されていない場合、または有効な結果に変換できない場合、MONTH 関数はエラーを返します。
  
戻り値は、システムの現在の [地域別設定] に設定されている短い形式の日付で書式設定されます。
  
MONTH 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表す式の単一の数値も受け入れられます。 
  
## <a name="example-1"></a>例 1

MONTH("May 30, 1999 13:45:24")
  
5 を返します。
  
## <a name="example-2"></a>例 2

MONTH(DATEVALUE("May 30, 1999")+7 ed.)
  
6 を返します。
  
## <a name="example-3"></a>例 3

MONTH(35580.6337)
  
5 を返します。
  

