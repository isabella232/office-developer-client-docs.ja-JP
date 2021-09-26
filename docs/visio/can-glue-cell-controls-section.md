---
title: '[Can Glue] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
ms.localizationpriority: medium
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: コントロール ハンドルを他の図形に接着できるかを指定します。
ms.openlocfilehash: 751a9b28351965b0239c34b6195e75f89d5f1b7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613129"
---
# <a name="can-glue-cell-controls-section"></a>[Can Glue] セル ([Controls] セクション)

コントロール ハンドルを他の図形に接着できるかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | コントロール ハンドルを接着できます。  <br/> |
| FALSE  <br/> | コントロール ハンドルを接着できません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Can Glue] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | コントロール。  *name*  .CanGluewhere コントロール。  *name*  は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Can Glue] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl**  +  *i* *=* 0, 1, 2, ...  <br/> |
| セル インデックス:  <br/> |**visCtlGlue** <br/> |
   

