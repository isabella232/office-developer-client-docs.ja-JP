---
title: '[Prompt] セル ([User-Defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
ms.localizationpriority: medium
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。 アプリケーションは、プロンプト テキストを自動的に二重引用符 () で囲み、テキスト文字列を示します。 等号 (=) を入力し、二重引用符を省略した場合は、アプリケーションが評価する数式をこのセルに入力できます。
ms.openlocfilehash: 158925e01f710053998189367a9182b2b3eda4b0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623181"
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
   

