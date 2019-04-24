---
title: '[Print] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: レイヤーに属している図形が印刷可能かどうかを指定します。
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356183"
---
# <a name="print-cell-layers-section"></a>[Print] セル ([Layers] セクション)

レイヤーに属している図形が印刷可能かどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形を印刷できます。  <br/> |
|FALSE  <br/> |図形を印刷できません。  <br/> |
   
## <a name="remarks"></a>解説

この値は、[**レイヤー プロパティ**] ダイアログ ボックスの [**印刷**] オプションを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Print] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |<1>、2、3のよう** に、[ *i* ] を印刷します。  <br/> |
   
プログラムから、インデックスによって [Print] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visDocPreviewScope** <br/> |
   

