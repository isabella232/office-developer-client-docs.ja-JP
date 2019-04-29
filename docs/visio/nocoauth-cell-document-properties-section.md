---
title: '[NoCoauth] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: microsoft SharePoint 2013 サーバーまたは microsoft OneDrive に保存されているドキュメントを共同編集セッションで同時に複数の作成者が編集できるようにするかどうかを設定します。
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420515"
---
# <a name="nocoauth-cell-document-properties-section"></a>[NoCoauth] セル ([ドキュメントのプロパティ] セクション)

microsoft SharePoint 2013 サーバーまたは microsoft OneDrive に保存されているドキュメントを共同編集セッションで同時に複数の作成者が編集できるようにするかどうかを設定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |ドキュメントは共同編集できません。開かれると編集用にロックされます。  <br/> |
|FALSE  <br/> |ドキュメントは共同編集できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**NoCoauth**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [nocoauth]  <br/> |
   
プログラムから、インデックスによって [**NoCoauth**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocNoCoauth** <br/> |
   

