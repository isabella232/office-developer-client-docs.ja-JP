---
title: '[ReplaceCopyCells] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: 図形の置換操作中に、古い図形から置換後の図形にコピーされるシェイプシート内のセル一覧を示します。
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806189"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>[ReplaceCopyCells] セル ([図形動作の変更] セクション)

図形の置換操作中に、古い図形から置換後の図形にコピーされるシェイプシート内のセル一覧を示します。 
  
## <a name="remarks"></a>Remarks

置換後のマスター シェイプは、関数の各引数がセルの参照になる [**ReplaceCopyCells**] セル内に**DEPENDSON** 関数呼び出しを格納する必要があります。これらのセルは、セルがシェイプシート内のどこにあるかは関係なく、古い図形から、図形の置換操作の結果である図形にコピーされます。 
  
他のセルを参照する値および/または数式は、作成した図形にコピーされます。作成した図形に参照先のセルがない場合、コピーされたセルには値のみが格納されます。 
  
[**ReplaceCopyCells**] セルの参照は、[**保護**] セクションで定義されたセル、[**ReplaceLockFormat**] セル、[**ReplaceLockShapeData**] セル、および [**ReplaceLockText**] セルの保護設定に優先します。 
  
別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReplaceCopyCells**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReplaceCopyCells  <br/> |
   
プログラムから、インデックスによって [**ReplaceCopyCells**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowReplaceBehaviors** <br/> |
| セル インデックス:  <br/> |**visReplaceCopyCells** <br/> |
   

