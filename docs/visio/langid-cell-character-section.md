---
title: '[LangID] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: テキストの記入に使用した言語を示します。
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326923"
---
# <a name="langid-cell-character-section"></a>[LangID] セル ([Character] セクション)

テキストの記入に使用した言語を示します。 
  
## <a name="remarks"></a>解説

Microsoft Office アプリケーションがサポートしている言語の一覧は、[[DocLangID](doclangid-cell-document-properties-section.md)] セル ([Document Properties] セクション) を参照してください。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | <1> [ *i* ]、 *i* =、2、3...  <br/> |
   
プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visCharacterLangID** <br/> |
   

