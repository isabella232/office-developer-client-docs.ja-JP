---
title: RGB 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
ms.localizationpriority: medium
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: ドキュメントのカラー パレット内のインデックスを表す値を返します。 赤、緑、青の各成分で色を指定します。各コンポーネントは、0 ~ 255 の範囲の数値、またはそのような数値に評価される式です。
ms.openlocfilehash: 9705d0e4c881a2d98e176a9982bbc7a95140755c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573524"
---
# <a name="rgb-function-visioshapesheet"></a>RGB 関数 (VisioShapeSheet)

ドキュメントのカラー パレット内のインデックスを表す値を返します。 赤、緑、青の各成分で色を指定します。各コンポーネントは、0 ~ 255 の範囲の数値、またはそのような数値に評価される式です。 
  
## <a name="syntax"></a>構文

RGB(** *red* **, ** *green* **, ** *blue* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _red_ <br/> |必須かどうか  <br/> |**数値** <br/> |赤のコンポーネントを指定します。  <br/> |
| _green_ <br/> |必須かどうか  <br/> |**数値** <br/> |緑のコンポーネントを指定します。  <br/> |
| _blue_ <br/> |必須かどうか  <br/> |**Nmber** <br/> |青のコンポーネントを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

関数が返す色が現在の図面のカラー パレットにない場合、その色がパレットに追加されます。
  
次の表は、標準色とその色に対する赤、緑、青コンポーネントの値の一覧です。
  
|**Color**|**赤の値**|**緑の値**|**青の値**|
|:-----|:-----|:-----|:-----|
|黒  <br/> |0  <br/> |0  <br/> |0  <br/> |
|青  <br/> |0  <br/> |0  <br/> |255  <br/> |
|緑  <br/> |0  <br/> |255  <br/> |0  <br/> |
|シアン  <br/> |0  <br/> |255  <br/> |255  <br/> |
|赤  <br/> |255  <br/> |0  <br/> |0  <br/> |
|マゼンダ  <br/> |255  <br/> |0  <br/> |255  <br/> |
|黄色  <br/> |255  <br/> |255  <br/> |0  <br/> |
|白  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>例 1

RGB(0,0,255)
  
青色に対するインデックスを返します。
  
## <a name="example-2"></a>例 2

RGB(RED(Sheet.1!FillForegnd),120,0)
  
Sheet.1 の前景の塗りつぶし色に適用されている赤コンポーネントを使用して、色のインデックスを返します。
  

