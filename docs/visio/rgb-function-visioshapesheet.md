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
description: ドキュメントのカラーパレット内のインデックスを表す値を返します。 赤、緑、青のコンポーネントで色を指定します。各要素は、0 ~ 255 の範囲の数値、またはそのような数値に評価される式です。
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326741"
---
# <a name="rgb-function-visioshapesheet"></a>RGB 関数 (VisioShapeSheet)

ドキュメントのカラーパレット内のインデックスを表す値を返します。 赤、緑、青のコンポーネントで色を指定します。各要素は、0 ~ 255 の範囲の数値、またはそのような数値に評価される式です。 
  
## <a name="syntax"></a>構文

RGB (* **赤** *、* * *green* * *、* * *blue* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _red_ <br/> |必須  <br/> |**数値** <br/> |赤のコンポーネントを指定します。  <br/> |
| _green_ <br/> |必須  <br/> |**数値** <br/> |緑のコンポーネントを指定します。  <br/> |
| _blue_ <br/> |必須  <br/> |**Nmber** <br/> |青のコンポーネントを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>解説

関数が返す色が現在の図面のカラー パレットにない場合、その色がパレットに追加されます。
  
次の表は、標準色とその色に対する赤、緑、青コンポーネントの値の一覧です。
  
|**色**|**赤の値**|**緑の値**|**青の値**|
|:-----|:-----|:-----|:-----|
|黒  <br/> |.0  <br/> |.0  <br/> |.0  <br/> |
|青  <br/> |.0  <br/> |.0  <br/> |255  <br/> |
|緑  <br/> |.0  <br/> |255  <br/> |.0  <br/> |
|シアン  <br/> |.0  <br/> |255  <br/> |255  <br/> |
|赤  <br/> |255  <br/> |.0  <br/> |.0  <br/> |
|マゼンダ  <br/> |255  <br/> |.0  <br/> |255  <br/> |
|黄色  <br/> |255  <br/> |255  <br/> |.0  <br/> |
|白  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>例 1

RGB (0、0255)
  
青色に対するインデックスを返します。
  
## <a name="example-2"></a>例 2

RGB (赤 (Sheet. 1![fillforegnd])、120、0)
  
Sheet.1 の前景の塗りつぶし色に適用されている赤コンポーネントを使用して、色のインデックスを返します。
  

