---
title: '[PreviewScope] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: 図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806098"
---
# <a name="previewscope-cell-document-properties-section"></a>[PreviewScope] セル ([ドキュメントのプロパティ] セクション)

図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。
  
|**値**|**プレビューの範囲**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 最初のページ  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | なし  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | すべてのページ  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>注釈

[**概要**] タブ、[**プロパティ**] ダイアログ ボックスでこの値を設定することもできます ( **Office**ボタンをクリックして、[**情報**] タブをクリックして、**ドキュメントのプロパティ**] をクリックし、[**詳細プロパティ**] をクリック) します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PreviewScope] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PreviewScope  <br/> |
   
プログラムから、インデックスによって [PreviewScope] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocPreviewScope** <br/> |
   

