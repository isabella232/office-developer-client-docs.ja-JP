---
title: '[IndFirst] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: 図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805569"
---
# <a name="indfirst-cell-paragraph-section"></a>[IndFirst] セル ([段落] セクション)

図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。
  
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IndFirst] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Para.IndFirst [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [IndFirst] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visIndentFirst** <br/> |
   

