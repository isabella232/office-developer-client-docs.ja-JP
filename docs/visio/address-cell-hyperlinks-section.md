---
title: '[Address] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: 移動先の URL アドレス、ファイル名、または UNC パスを指定します。
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804780"
---
# <a name="address-cell-hyperlinks-section"></a>[Address] セル ([ハイパーリンク] セクション)

移動先の URL アドレス、ファイル名、または UNC パスを指定します。
  
[**プロパティ**] ダイアログ ボックスの [**ハイパーリンクの基点**] ボックス [**概要**] タブでドキュメントに定義された基本パスに基づく相対パスとしてアドレスを指定することができます ([**ファイル**] タブをクリックして、[**情報**] をクリックして、をクリックして * * プロパティ * *、、[**詳細プロパティ**] をクリックし、)。 ドキュメントには、基本パスがなければ、アプリケーションは、文書へのパスに基づいて移動します。 ドキュメントが保存されていない場合、ハイパーリンクは未定義です。
  
## <a name="remarks"></a>注釈

[Address] セルの値は [**ハイパーリンク**] ダイアログ ボックスでも設定できます (このダイアログ ボックスを表示するには、[**挿入**] タブで [**ハイパーリンク**] をクリックします)。 
  
プログラムから、インデックスによって [Address] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *名*です。場所のアドレスのハイパーリンクです。 *ハイパーリンク行の名前します。*  <br/> |
   
取得する、[Address] セルへの参照を名前で別の数式からまたはプログラムでは、 **CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visHLinkAddress** <br/> |
   

