---
title: '[PageTopMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: 印刷ページの上余白を指定します。
ms.openlocfilehash: 1b7be63e3f21365231120c602d8edfe1dc727f88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805969"
---
# <a name="pagetopmargin-cell-print-properties-section"></a>[PageTopMargin] セル ([印刷のプロパティ] セクション)

印刷ページの上余白を指定します。
  
## <a name="remarks"></a>備考

この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.25 インチなら、ページ単位がフィートの場合でも、この余白は 0.25 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageTopMargin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PageTopMargin  <br/> |
   
プログラムから、インデックスによって [PageTopMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesTopMargin** <br/> |
   

