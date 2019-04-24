---
title: '[PaperKind] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: ページを印刷する用紙の種類を指定します。
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327063"
---
# <a name="paperkind-cell-print-properties-section"></a>[PaperKind] セル ([Print Properties] セクション)

ページを印刷する用紙の種類を指定します。
  
## <a name="remarks"></a>解説

この設定は、[**デザイン**] タブの [**ページ設定**] 矢印をクリックし、[印刷**設定**] タブの [**設定**] ボタンをクリックすると表示される、[**印刷設定**] ダイアログボックスの [**用紙サイズ**] の設定に対応しています。 
  
このセルの数値は、Microsoft Windows の DMPAPER ファイルで用紙を選択するために定義されている定数 (プレフィックスは) に対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageKind] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[paperkind]  <br/> |
   
プログラムから、インデックスによって [PaperKind] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

