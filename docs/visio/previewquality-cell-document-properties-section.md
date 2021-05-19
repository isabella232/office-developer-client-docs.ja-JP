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
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416819"
---
# <a name="previewquality-cell-document-properties-section"></a>[PreviewQuality] セル ([Document Properties] セクション)

図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。
  
|**値**|**プレビューの品質**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 下書き  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | 詳細  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>注釈

この値は、[プロパティ] ダイアログボックスの [概要] タブで設定することもできます **([Office]** ボタンをクリックし、[情報] タブをクリックし、[ドキュメントのプロパティ] をクリックし、[詳細プロパティ] をクリック **します**)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PreviewQuality] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PreviewQuality  <br/> |
   
プログラムから、インデックスによって [PreviewQuality] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocPreviewQuality** <br/> |
   

