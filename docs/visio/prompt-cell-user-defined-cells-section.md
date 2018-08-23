---
title: '[Prompt] セル ([User-Defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。 アプリケーションでは、プロンプトのテキストがテキスト文字列であることを示すには引用符 () で自動的に囲まれます。 等号 (=) を入力して引用符を省略した場合は、このアプリケーションを評価するセルの数式を入力することができます。
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806126"
---
# <a name="prompt-cell-user-defined-cells-section"></a>[Prompt] セル ([ユーザー定義セル] セクション)

ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。プロンプト テキストは自動的に引用符 (" ") で囲まれ、テキスト文字列として認識されます。このセルに数式を入力するには、等号 (=) を入力して引用符を省略します。これにより、数式はアプリケーションによって評価されます。
  
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Prompt] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ユーザーです。  *名*です。プロンプトの場所のユーザーです。  *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Prompt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionUser** <br/> |
| 行インデックス:  <br/> |**visRowUser +***i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visUserPrompt** <br/> |
   

