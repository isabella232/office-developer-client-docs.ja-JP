---
title: '[Prompt] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: '[図形データ] ウィンドウ内の値の上にマウスを置いたときにヒントとして表示される説明や手順のテキストを指定します。'
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806109"
---
# <a name="prompt-cell-shape-data-section"></a>[Prompt] セル ([Shape Data] セクション)

[**図形データ**] ウィンドウ内の値の上にマウスを置いたときにヒントとして表示される説明や手順のテキストを指定します。 
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Prompt] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | プロペラです。 *名*です。*という行の名前*の入力を求める  <br/> |
   
プログラムから、インデックスによって [Prompt] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp +***i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCustPropsPrompt** <br/> |
   

