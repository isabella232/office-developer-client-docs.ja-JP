---
title: '[ConFixedCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: コネクタの経路の変更方法を指定します。
ms.openlocfilehash: 448e721d8dd6e287c61488e28b875f76d0fa2977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805083"
---
# <a name="confixedcode-cell-shape-layout-section"></a>[ConFixedCode] セル ([Shape Layout] セクション)

コネクタの経路の変更方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |自由に経路変更します。  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |必要な (手動ルーティング) に応じて経路を変更します。  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |経路変更しません。  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |交差時に経路変更します。  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |内部使用のみ。   <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |内部使用のみ。   <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |内部使用のみ。   <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>備考

設定できますでは、このセルの値、動的コネクタを**図形のデザイン**] で [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**動作**をクリックして、[**コネクタ**] タブをクリックします。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ConFixedCode] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ConFixedCode  <br/> |
   
プログラムから、インデックスによって [ConFixedCode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOConFixedCode** <br/> |
   

