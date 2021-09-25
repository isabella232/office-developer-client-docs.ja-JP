---
title: '[LockPreview] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
ms.localizationpriority: medium
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: 図面を保存するたびにプレビューを保存するかどうかを指定します。
ms.openlocfilehash: 48ec2c7f8ae49bae5a8e2bfe2d4534a48a681807
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615873"
---
# <a name="lockpreview-cell-document-properties-section"></a>[LockPreview] セル ([Document Properties] セクション)

図面を保存するたびにプレビューを保存するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図面を保存するたびにプレビューを保存しません。  <br/> |
| FALSE  <br/> | 図面を保存するたびにプレビューを保存します。  <br/> |
   
## <a name="remarks"></a>注釈

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
   

