---
title: '[ImgOffsetY] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm455
localization_priority: Normal
ms.assetid: 3b2991aa-4722-fe3b-39c5-02d38c4c7efc
description: オブジェクトの枠の原点からオブジェクトを垂直方向へオフセットする距離を指定します。既定値は 0 です。[トリミング ツール] を使用してオブジェクトをパンすると、この値が変化します。
ms.openlocfilehash: 908972216a24370bc48990ddc99a36da9274d648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406739"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a>[ImgOffsetY] セル ([Foreign Image Info] セクション)

オブジェクトの枠の原点からオブジェクトを垂直方向へオフセットする距離を指定します。既定値は 0 です。**[トリミング ツール]** を使用してオブジェクトをパンすると、この値が変化します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgOffsetY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ImgOffsetY  <br/> |
   
プログラムから、インデックスによって [ImgOffsetY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowForeign** <br/> |
| セル インデックス:  <br/> |**visFrgnImgOffsetY** <br/> |
   

