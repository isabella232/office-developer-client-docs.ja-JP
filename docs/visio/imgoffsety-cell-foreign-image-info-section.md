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
ms.openlocfilehash: 2930aa092a2b776ceb0c9c4677f7e5da7f5dcdda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805566"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a>[ImgOffsetY] セル ([外部画像情報] セクション)

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
   

