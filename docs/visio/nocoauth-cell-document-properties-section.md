---
title: '[NoCoauth] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Microsoft SharePoint 2013 サーバーまたは Microsoft OneDrive に保存されているドキュメントを、共同編集セッションで複数の作成者が同時に編集できるかどうかを設定します。
ms.openlocfilehash: 505617992f2a35e0603ed676b1e6dcb1fa1b5511
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562973"
---
# <a name="nocoauth-cell-document-properties-section"></a>[NoCoauth] セル ([ドキュメントのプロパティ] セクション)

Microsoft SharePoint 2013 サーバーまたは Microsoft OneDrive に保存されているドキュメントを、共同編集セッションで複数の作成者が同時に編集できるかどうかを設定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |ドキュメントは共同編集できません。開かれると編集用にロックされます。  <br/> |
|FALSE  <br/> |ドキュメントは共同編集できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**NoCoauth**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | NoCoauth  <br/> |
   
プログラムから、インデックスによって [**NoCoauth**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocNoCoauth** <br/> |
   

