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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408447"
---
# <a name="paperkind-cell-print-properties-section"></a>[PaperKind] セル ([Print Properties] セクション)

ページを印刷する用紙の種類を指定します。
  
## <a name="remarks"></a>注釈

この設定は、[印刷設定] ダイアログ ボックスの [用紙サイズ]設定に対応します([デザイン] タブの[ページ設定] 矢印をクリックし、[印刷セットアップ] タブで [セットアップ] ボタンを **クリック** します)。 
  
このセル内の数値は、Microsoft Windows wingdi.h ファイルの用紙選択に対して定義された定数 (DMPAPER のプレフィックス) にマップされます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageKind] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PaperKind  <br/> |
   
プログラムから、インデックスによって [PaperKind] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

