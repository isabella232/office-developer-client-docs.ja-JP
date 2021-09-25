---
title: HOUR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
ms.localizationpriority: medium
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: 日付または式の日の時間を表す 0 ~ 23 の整数を返します。
ms.openlocfilehash: 152dc3bc995ebfdcfe3f419f51d761f9ff054f7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628200"
---
# <a name="hour-function-visioshapesheet"></a>HOUR 関数 (VisioShapeSheet)

日付または式の日の時間を表す 0 ~ 23 の  _整数を_ 返  _します_。
  
## <a name="syntax"></a>構文

HOUR(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須かどうか  <br/> |**さまざま** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> | 現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
## <a name="remarks"></a>注釈

datetime および *式の日付**コンポーネントは* 破棄されます。 
  
数値は四捨五入されません。 datetime  *が見つからない*  か、有効な結果に変換できない場合、関数はエラーを返します。 
  
戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。 
  
HOUR 関数は、結果の小数部分が午前 0 時からの 1 日の小数部を表す式の単一の数値も受け入れられます。 
  
## <a name="example-1"></a>例 1

HOUR("15:45")
  
15 を返します。
  
## <a name="example-2"></a>例 2

HOUR("1997 年 5 月 30 日 15:45:24")
  
15 を返します。
  
## <a name="example-3"></a>例 3

HOUR(0.5)
  
12 を返します。
  
## <a name="example-4"></a>例 4

HOUR("5/30/1997")
  
0 を返します。
  

