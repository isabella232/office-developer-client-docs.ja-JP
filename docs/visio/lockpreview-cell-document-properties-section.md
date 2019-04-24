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
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348329"
---
# <a name="lockpreview-cell-document-properties-section"></a>[LockPreview] セル ([Document Properties] セクション)

図面を保存するたびにプレビューを保存するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図面を保存するたびにプレビューを保存しません。  <br/> |
| FALSE  <br/> | 図面を保存するたびにプレビューを保存します。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockPreview] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [lockpreview]  <br/> |
   
プログラムから、インデックスによって [LockPreview] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocLockPreview** <br/> |
   

