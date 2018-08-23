---
title: '[LangID] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: 図形データ値の記入に使用した言語を示します。
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805674"
---
# <a name="langid-cell-shape-data-section"></a>[LangID] セル ([図形データ] セクション)

図形データ値の記入に使用した言語を示します。 
  
## <a name="remarks"></a>備考

Microsoft Office system のアプリケーションがサポートしている言語の一覧は、[[DocLangID]](doclangid-cell-document-properties-section.md) セル ([Document Properties] セクション) を参照してください。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | プロペラです。 *名*です。LangID でプロペラです。 *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCustPropsLangID** <br/> |
   

