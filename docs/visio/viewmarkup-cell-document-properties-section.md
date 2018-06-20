---
title: '[ViewMarkup] セル ([Document Properties] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: 図面ウィンドウに校正履歴を表示するかどうかを指定します。
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806780"
---
# <a name="viewmarkup-cell-document-properties-section"></a>[ViewMarkup] セル ([Document Properties] セクション

図面ウィンドウに校正履歴を表示するかどうかを指定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図面ウィンドウに校正履歴を表示します。  <br/> |
|FALSE  <br/> |校正履歴を表示しません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

 校正履歴の記録を有効にすると ([addmarkup] セルが TRUE)、ViewMarkup セルが自動的に TRUE に設定し、校正履歴の記録がオフになっている後でも TRUE のまま ([addmarkup] セルでは FALSE です)。 AddMarkup セルが TRUE の場合に、[ViewMarkup] セルの値は無視されます。 
  
図面にコメントを挿入した場合、校正履歴の記録機能がオンかどうかに関わらず、[ViewMarkup] セルは TRUE に設定されます。[ViewMarkup] セルが TRUE でなければ、図面内にコメントが表示されません。
  
このセルは、[**校閲**] タブには、**マークアップ**のグループ内の**コメントの表示**コマンドに対応します。 
  
取得する、[ViewMarkup] セルへの参照名を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ViewMarkup  <br/> |
   
プログラムから、インデックスによって [ViewMarkup] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowDoc** <br/> |
|セル インデックス:  <br/> |**visDocViewMarkup** <br/> |
   

