---
title: RGB 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: 図面のカラー パレットのインデックスを表す値を返します。 範囲 0 ~ 255 の範囲の数字をそれぞれ、赤、緑、および青コンポーネントを使用して色を指定します。
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806233"
---
# <a name="rgb-function-visioshapesheet"></a>RGB 関数 (VisioShapeSheet)

図面のカラー パレットのインデックスを表す値を返します。 範囲 0 ~ 255 の範囲の数字をそれぞれ、赤、緑、および青コンポーネントを使用して色を指定します。 
  
## <a name="syntax"></a>構文

RGB (* **赤** *、* **緑** *、* **ブルー* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _red_ <br/> |必須  <br/> |**番号** <br/> |赤のコンポーネントを指定します。  <br/> |
| _green_ <br/> |必須  <br/> |**番号** <br/> |緑のコンポーネントを指定します。  <br/> |
| _blue_ <br/> |必須  <br/> |**番号** <br/> |青のコンポーネントを指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

数値
  
## <a name="remarks"></a>注釈

関数が返す色が現在の図面のカラー パレットにない場合、その色がパレットに追加されます。
  
次の表は、標準色とその色に対する赤、緑、青コンポーネントの値の一覧です。
  
|**色**|**赤の値**|**緑の値**|**青の値**|
|:-----|:-----|:-----|:-----|
|黒  <br/> |0  <br/> |0  <br/> |0  <br/> |
|青  <br/> |0  <br/> |0  <br/> |255  <br/> |
|緑  <br/> |0  <br/> |255  <br/> |0  <br/> |
|シアン  <br/> |0  <br/> |255  <br/> |255  <br/> |
|赤  <br/> |255  <br/> |0  <br/> |0  <br/> |
|マゼンダ  <br/> |255  <br/> |0  <br/> |255  <br/> |
|黄  <br/> |255  <br/> |255  <br/> |0  <br/> |
|白  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>例 1

RGB(0,0,255)
  
青色に対するインデックスを返します。
  
## <a name="example-2"></a>例 2

RGB (赤 (Sheet.1!FillForegnd)、120, 0)
  
Sheet.1 の前景の塗りつぶし色に適用されている赤コンポーネントを使用して、色のインデックスを返します。
  

