---
title: '[Type] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: テキスト フィールドの値に対してデータの種類を指定します。
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806705"
---
# <a name="type-cell-text-fields-section"></a>[Type] セル ([テキスト フィールド] セクション)

テキスト フィールドの値に対してデータの種類を指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |文字列。  <br/> |
|2  <br/> |数値。日付、時刻、期間、通貨の値の他、スカラー、寸法、角度も含まれます。書式形式は [Format] セルで指定します。  <br/> |
|5  <br/> |日付または時刻の値。日、月、年、および秒、分、時間、または日付と時刻の組み合わせを表示します。書式形式は [Format] セルで指定します。  <br/> |
|6  <br/> |期間の値。経過時間を表示します。書式形式は [Format] セルで指定します。  <br/> |
|7  <br/> |通貨の値。システムに適用されている現在の地域別設定を使用します。書式形式は [Format] セルで指定します。  <br/> |
   
## <a name="remarks"></a>注釈

**フィールド**] ダイアログ ボックスを使用してこのセルの値を設定することもできます (図形を選択して、[**挿入**] タブの [**テキスト**] で、[**フィールド**] をクリック) します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Type] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Fields.Type [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Type] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionTextField** <br/> |
|行インデックス:  <br/> |**visRowField** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visFieldType** <br/> |
   

