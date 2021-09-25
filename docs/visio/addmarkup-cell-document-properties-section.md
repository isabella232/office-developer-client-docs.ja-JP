---
title: '[AddMarkup] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
ms.localizationpriority: medium
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: 図面が校正履歴用にチェックされているかどうかを示します。
ms.openlocfilehash: f97dc836d7307c8a35fe0db8f1cd73035c52ac94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560152"
---
# <a name="addmarkup-cell-document-properties-section"></a>[AddMarkup] セル ([Document Properties] セクション)

図面が校正履歴用にチェックされているかどうかを示します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図面はチェックされています。  <br/> |
|FALSE  <br/> |図面はチェックされていません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

AddMarkup セルが TRUE に設定されている場合、校閲者が校正履歴を追加しており、変更はオリジナルの図面ページではなく校正履歴のオーバーレイ ページに適用されます。 AddMarkup セルが FALSE に設定されている場合、校正履歴の記録はオフになっており、変更はオリジナルの図面ページに適用されます。
  
> [!NOTE]
> GUARD 関数を使用すると、ドキュメントのマークアップを防止できます。 [AddMarkup] セルに数式 =GUARD(FALSE) が含まれている場合、[マークアップの追跡] **コマンドは** 無効になります。 
  
この設定は、[**校閲**] タブの [**校正履歴**] グループにある [**校正履歴の記録**] コマンドに相当します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AddMarkup] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |AddMarkup  <br/> |
   
プログラムから、インデックスによって [AddMarkup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowDoc** <br/> |
|セル インデックス:  <br/> |**visDocAddMarkup** <br/> |
   

