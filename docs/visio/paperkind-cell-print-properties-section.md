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
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805974"
---
# <a name="paperkind-cell-print-properties-section"></a>[PaperKind] セル ([Print Properties] セクション)

ページを印刷する用紙の種類を指定します。
  
## <a name="remarks"></a>注釈

この設定は、[**印刷設定**] ダイアログ ボックスで**用紙サイズ**の設定に対応して ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**プリンターの設定**] タブで、**設定**ボタンをクリック) します。 
  
用紙の Microsoft Windows wingdi.h ファイル内のこのセルにマップが付いて DMPAPER) の定数に含まれる数値が定義されています。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PaperKind] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PaperKind  <br/> |
   
プログラムから、インデックスによって [PaperKind] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

