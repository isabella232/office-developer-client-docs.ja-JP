---
title: '[Checked] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438331"
---
# <a name="checked-cell-actions-section"></a>[Checked] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |チェック マークが表示されます。  <br/> |
|FALSE  <br/> |チェック マークが表示されません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Checked] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション. *名前*です。アクションを確認しました。 *name*は、Actions 行の名前です。  <br/> |
   
プログラムから、インデックスによって [Checked] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* = ** 0、1、2、...  <br/> |
|セル インデックス:  <br/> |**visActionChecked** <br/> |
   

