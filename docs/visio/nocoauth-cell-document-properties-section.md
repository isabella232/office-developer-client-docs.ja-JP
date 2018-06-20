---
title: '[NoCoauth] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Microsoft SharePoint 2013 のサーバーまたはマイクロソフトの OneDrive に格納されているドキュメントにことができます coauthoring のセッションで同時に複数の作成者によって編集かどうかを設定します。
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805925"
---
# <a name="nocoauth-cell-document-properties-section"></a>[NoCoauth] セル ([ドキュメントのプロパティ] セクション)

Microsoft SharePoint 2013 のサーバーまたはマイクロソフトの OneDrive に格納されているドキュメントにことができます coauthoring のセッションで同時に複数の作成者によって編集かどうかを設定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |ドキュメントは共同編集できません。開かれると編集用にロックされます。  <br/> |
|FALSE  <br/> |ドキュメントは共同編集できます。  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **NoCoauth** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | NoCoauth  <br/> |
   
プログラムから、インデックスによって [ **NoCoauth** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocNoCoauth** <br/> |
   

