---
title: '[LockPreview] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: 図面を保存するたびにプレビューを保存するかどうかを指定します。
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805765"
---
# <a name="lockpreview-cell-document-properties-section"></a>[LockPreview] セル ([ドキュメントのプロパティ] セクション)

図面を保存するたびにプレビューを保存するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図面を保存するたびにプレビューを保存しません。  <br/> |
| FALSE  <br/> | 図面を保存するたびにプレビューを保存します。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockPreview] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockPreview  <br/> |
   
プログラムから、インデックスによって [LockPreview] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocLockPreview** <br/> |
   

