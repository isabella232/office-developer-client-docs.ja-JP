---
title: '[ReadOnly] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
ms.localizationpriority: medium
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。
ms.openlocfilehash: af4a2d4945032a100d39440c9c3bed427d310c06
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559739"
---
# <a name="readonly-cell-actions-section"></a>[ReadOnly] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |アクションはメニューに表示されますが、読み取り専用です。  <br/> |
|FALSE  <br/> |アクションはメニューに表示され、選択できます (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

アクションが読み取り専用の場合、アクション タグ メニューまたはショートカット メニューに表示されますが、選択できません。 灰色表示にはなりませんが、色が付いた背景の上にラベルのように表示されます。 そのメニュー項目を灰色表示にするには、[Disabled] セルを使用します。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [ReadOnly] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション。 *name*  .ReadOnlywhere Actions.  *name*  は [アクション] 行の名前です。  <br/> |
   
プログラムから、インデックスによって [ReadOnly] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visActionReadOnly** <br/> |
   

