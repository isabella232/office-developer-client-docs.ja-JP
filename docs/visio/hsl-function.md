---
title: HSL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
ms.localizationpriority: medium
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: ドキュメントのカラー パレット内のインデックスを表す値を返します。 色相、彩度、光度の各成分で色を指定します。
ms.openlocfilehash: 1cf21354c5c514327b5cf3a8bd0fd76e5bd099f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570478"
---
# <a name="hsl-function"></a>HSL 関数

ドキュメントのカラー パレット内のインデックスを表す値を返します。 色相、彩度、光度の各成分で色を指定します。
  
## <a name="syntax"></a>構文

HSL(** *hue* **, ** *彩* 度 **, ** *明度* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _hue_ <br/> |必須かどうか  <br/> |**数値** <br/> |色の色合いです。0 ～ 239 (0 と 239 を含む) の範囲の数値、またはこの範囲の数値に評価される式を指定します。  <br/> |
| _彩度_ <br/> |必須かどうか  <br/> |**数値** <br/> |色の彩度です。0 ～ 240 (0 と 240 を含む) の範囲の数値、またはこの範囲の数値に評価される式を指定します。  <br/> |
| _明度_ <br/> |必須かどうか  <br/> |**数値** <br/> | 色の明度です。0 ～ 240 (0 と 240 を含む) の範囲の数値、またはこの範囲の数値に評価される式を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

関数によって返される色が現在の図面のカラー パレットにない場合、その色が図面で使用できる色の一覧に追加されます。 
  
次の表は、標準の色とその色に対する色合い、彩度、明度の値の一覧です。 
  
|**Color**|**色合いの値**|**彩度の値**|**明度の値**|
|:-----|:-----|:-----|:-----|
|黒  <br/> |0  <br/> |0  <br/> |24  <br/> |
|青  <br/> |160  <br/> |240  <br/> |120  <br/> |
|緑  <br/> |80  <br/> |240  <br/> |120  <br/> |
|シアン  <br/> |120  <br/> |240  <br/> |120  <br/> |
|赤  <br/> |0  <br/> |240  <br/> |120  <br/> |
|マゼンダ  <br/> |200  <br/> |240  <br/> |120  <br/> |
|黄  <br/> |40  <br/> |240  <br/> |120  <br/> |
|ホワイト  <br/> |0  <br/> |0  <br/> |240  <br/> |
   
## <a name="example-1"></a>例 1

HSL(160,240,120)
  
青色に対するインデックスを返します。
  
## <a name="example-2"></a>例 2

HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))
  
前景の塗りつぶしの色に対して明度を高くしたときの、色のインデックスを返します。
  

