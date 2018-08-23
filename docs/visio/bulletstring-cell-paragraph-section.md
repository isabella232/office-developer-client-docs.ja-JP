---
title: '[BulletString] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: 箇条書きのスタイルをカスタマイズできます。
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804948"
---
# <a name="bulletstring-cell-paragraph-section"></a>[BulletString] セル ([段落] セクション)

箇条書きのスタイルをカスタマイズできます。 
  
## <a name="remarks"></a>注釈

スタイルを引用符で囲み、文字列として入力します。たとえば、"000." のように入力します。
  
このセルの値は、図形を右クリックして [**書式**] をポイントし、[**テキスト**]、[**箇条書き**] の順にクリックして設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BulletString] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Para.BulletStr [ *i* ]、 *i* = < 1 > では、2、3、.  <br/> |
   
プログラムから、インデックスによって [BulletString] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
|行インデックス:  <br/> |**visRowParagraph** +  *i* 、 *i* = 0、1、2、.  <br/> |
|セル インデックス:  <br/> |**visBulletString** <br/> |
   

