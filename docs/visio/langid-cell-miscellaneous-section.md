---
title: '[LangID] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: セル数式の作成に使用した言語を示します。
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805694"
---
# <a name="langid-cell-miscellaneous-section"></a>[LangID] セル ([その他] セクション)

セル数式の作成に使用した言語を示します。 
  
## <a name="remarks"></a>備考

Microsoft Office アプリケーションがサポートしている言語の一覧は、[[DocLangID](doclangid-cell-document-properties-section.md)] セル ([Document Properties] セクション) を参照してください。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LangID  <br/> |
   
プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visObjLangID** <br/> |
   

