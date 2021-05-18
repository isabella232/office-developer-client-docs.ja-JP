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
description: '[図形データ] ウィンドウで値の上にマウスを置いたときにヒントとして表示される説明または手順を示すテキストを指定します。'
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405486"
---
# <a name="prompt-cell-shape-data-section"></a>[Prompt] セル ([Shape Data] セクション)

[**図形データ**] ウィンドウで値の上にマウスを置いたときにヒントとして表示される説明または手順を示すテキストを指定します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Prompt] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Prop。  *Name*  .[名前]  *が行*  名のプロンプト  <br/> |
   
プログラムから、インデックスによって [Prompt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp +** *i*  *=*  0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCustPropsPrompt** <br/> |
   

