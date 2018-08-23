---
title: '[ImgHeight] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 枠内におけるオブジェクトのイメージの高さを指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805574"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>[ImgHeight] セル ([外部画像情報] セクション)

枠内におけるオブジェクトのイメージの高さを指定します。既定の数式は次のとおりです。
  
= 高さ\*1
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgHeight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Imgheight]  <br/> |
   
プログラムから、インデックスによって [ImgHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowForeign** <br/> |
| セル インデックス:  <br/> |**visFrgnImgHeight** <br/> |
   

