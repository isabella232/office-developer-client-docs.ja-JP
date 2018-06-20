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
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804776"
---
# <a name="addmarkup-cell-document-properties-section"></a>[AddMarkup] セル ([Document Properties] セクション)

図面が校正履歴用にチェックされているかどうかを示します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図面はチェックされています。  <br/> |
|FALSE  <br/> |図面はチェックされていません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

AddMarkup セルが TRUE に設定、レビュー担当者は、元の図面ページに、マークアップ オーバーレイ ページに追加のマークアップと変更が適用されます。 [Addmarkup] セルが FALSE で、校正履歴の記録とオフは、変更元の図面ページに適用されます。
  
> [!NOTE]
> GUARD 関数を使用して、ドキュメントのマークアップを防ぐことができます。 AddMarkup セルに数式が含まれている場合は = GUARD(FALSE)、校正履歴の**記録**を無効にします。 
  
この設定は、[**校閲**] タブには、**マークアップ**のグループで**校正履歴の記録**] コマンドの設定に対応します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [addmarkup] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Addmarkup]  <br/> |
   
プログラムから、インデックスによって [addmarkup] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowDoc** <br/> |
|セル インデックス:  <br/> |**visDocAddMarkup** <br/> |
   

