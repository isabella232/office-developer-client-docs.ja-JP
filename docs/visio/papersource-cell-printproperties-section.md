---
title: '[PaperSource] セル ([PrintProperties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: 用紙の給紙方法を指定します。
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805970"
---
# <a name="papersource-cell-printproperties-section"></a>[PaperSource] セル ([印刷のプロパティ] セクション)

用紙の給紙方法を指定します。 
  
## <a name="remarks"></a>注釈

この設定は、[**プリンターの設定**] ダイアログ ボックスの [**給紙**] の設定に対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**プリンターの設定**] タブで [**設定**] をクリックします)。
  
箱選択範囲の場合、Microsoft Windows wingdi.h ファイルで定義されているこのセルにマップ (DMBIN で始まる) の定数に含まれる数値たとえば、7 の値は、DMBIN_AUTO を表します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageSource] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PaperSource  <br/> |
   
プログラムから、インデックスによって [PaperSource] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

