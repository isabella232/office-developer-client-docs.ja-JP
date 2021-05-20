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
description: ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。 アプリケーションは、プロンプト テキストを自動的に二重引用符 () で囲み、テキスト文字列を示します。 等号 (=) を入力し、二重引用符を省略した場合は、アプリケーションが評価する数式をこのセルに入力できます。
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435727"
---
# <a name="prompt-cell-user-defined-cells-section"></a>[Prompt] セル ([User-Defined Cells] セクション)

ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。プロンプト テキストは自動的に引用符 (" ") で囲まれ、テキスト文字列として認識されます。このセルに数式を入力するには、等号 (=) を入力して引用符を省略します。これにより、数式はアプリケーションによって評価されます。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Prompt] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ユーザー。  *Name*  .[ユーザー] の場所を確認します。  *名前*  は行名です  <br/> |
   
プログラムから、インデックスによって [Prompt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionUser** <br/> |
| 行インデックス:  <br/> |**visRowUser +** *i*            *=*  0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visUserPrompt** <br/> |
   

