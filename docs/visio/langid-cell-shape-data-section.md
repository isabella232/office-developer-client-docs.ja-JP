---
title: '[LangID] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
ms.localizationpriority: medium
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: 図形データ値の記入に使用した言語を示します。
ms.openlocfilehash: c591b005f75e8644f751883738f1fd02cbd03853
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554524"
---
# <a name="langid-cell-shape-data-section"></a>[LangID] セル ([Shape Data] セクション)

図形データ値の記入に使用した言語を示します。 
  
## <a name="remarks"></a>注釈

Microsoft Office system のアプリケーションがサポートしている言語の一覧は、[[DocLangID]](doclangid-cell-document-properties-section.md) セル ([Document Properties] セクション) を参照してください。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Prop。  *name*  .Prop の場所の LangID。  *name*  は行名です  <br/> |
   
プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCustPropsLangID** <br/> |
   

