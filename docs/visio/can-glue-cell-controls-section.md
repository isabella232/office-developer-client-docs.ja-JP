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
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423294"
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
| セル名 :  <br/> | 管理.  *名前*です。CanGluewhere コントロール  *name*は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Can Glue] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* = ** 0、1、2、...  <br/> |
| セル インデックス:  <br/> |**visctlglue** <br/> |
   

