---
title: '[PreviewQuality] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: 図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806084"
---
# <a name="previewquality-cell-document-properties-section"></a>[PreviewQuality] セル ([Document Properties] セクション)

図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。
  
|**値**|**プレビューの品質**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | ドラフト  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | 詳細  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>備考

[**概要**] タブ、[**プロパティ**] ダイアログ ボックスでこの値を設定することもできます ( **Office**ボタンをクリックして、[**情報**] タブをクリックして、**ドキュメントのプロパティ**] をクリックし、[**詳細プロパティ**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PreviewQuality] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PreviewQuality  <br/> |
   
プログラムから、インデックスによって [PreviewQuality] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocPreviewQuality** <br/> |
   

