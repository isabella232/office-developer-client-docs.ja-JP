---
title: '[Can Glue] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: コントロール ハンドルを他の図形に接着できるかを指定します。
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804930"
---
# <a name="can-glue-cell-controls-section"></a>[Can Glue] セル ([Controls] セクション)

コントロール ハンドルを他の図形に接着できるかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | コントロール ハンドルを接着できます。  <br/> |
| FALSE  <br/> | コントロール ハンドルを接着できません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Can Glue] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 制御します。  *名*です。CanGluewhere を制御します。  *名*は、コントロールの行の名前です。  <br/> |
   
プログラムから、インデックスによって [Can Glue] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* 、 *i* = 0、1、2、.  <br/> |
| セル インデックス:  <br/> |**visCtlGlue** <br/> |
   

