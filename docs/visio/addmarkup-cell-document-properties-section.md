---
title: '[AddMarkup] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: 図面が校正履歴用にチェックされているかどうかを示します。
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338634"
---
# <a name="addmarkup-cell-document-properties-section"></a>[AddMarkup] セル ([Document Properties] セクション)

図面が校正履歴用にチェックされているかどうかを示します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図面はチェックされています。  <br/> |
|FALSE  <br/> |図面はチェックされていません (既定値)。  <br/> |
   
## <a name="remarks"></a>解説

AddMarkup セルが TRUE に設定されている場合、校閲者が校正履歴を追加しており、変更はオリジナルの図面ページではなく校正履歴のオーバーレイ ページに適用されます。 AddMarkup セルが FALSE に設定されている場合、校正履歴の記録はオフになっており、変更はオリジナルの図面ページに適用されます。
  
> [!NOTE]
> GUARD 関数を使用してドキュメントにマークアップを表示しないようにすることができます。 [addmarkup] セルに = GUARD (FALSE) という数式が含まれている場合は、[校正履歴の**記録**] コマンドは無効になります。 
  
この設定は、[**校閲**] タブの [**校正履歴**] グループにある [**校正履歴の記録**] コマンドに相当します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AddMarkup] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[addmarkup]  <br/> |
   
プログラムから、インデックスによって [AddMarkup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowDoc** <br/> |
|セル インデックス:  <br/> |**visDocAddMarkup** <br/> |
   

