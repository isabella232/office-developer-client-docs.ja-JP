---
title: '[Hyperlink] 行 ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: 図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
ms.openlocfilehash: 36b9b62f248e4f5b9407156a79fa674dc2e8f14d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329905"
---
# <a name="hyperlink-row-hyperlinks-section"></a>[Hyperlink] 行 ([Hyperlinks] セクション)

図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
  
[Hyperlink] 行の名前は Hyperlink. 次のセルに*名前*とが含まれます。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[説明](description-cell-hyperlinks-section.md) <br/> |ハイパーリンクを説明するテキスト文字列です。  <br/> |
|[Address](address-cell-hyperlinks-section.md) <br/> |移動先の URL アドレス、MS-DOS ファイル名、または UNC パスです。  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |リンク先のターゲット図面内での位置です。  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |URL の解決に使用される情報を渡す文字列です。  <br/> |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |ActiveX コンテナーで、ActiveX の図面として Microsoft Office Visio の図面を開く場合に、ターゲットとするフレームの名前です。既定では、空の文字列です。  <br/> |
|[[sortkey]](sortkey-cell-hyperlinks-section.md) <br/> |ハイパーリンクがショートカット メニューに表示されるときの順序を判別します。  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |ハイパーリンクを新しいウィンドウで開くかどうかを指定します。 TRUE の場合は、リンクされたページ、ドキュメント、または web サイトを新しいウィンドウで開きます。 既定値は "FALSE" です。  <br/> |
|[Default](default-cell-hyperlinks-section.md) <br/> |図形またはページに対する既定のハイパーリンクです。  <br/> |
|[可視](invisible-cell-hyperlinks-section.md) <br/> |ハイパーリンクがショートカット メニューに表示されるかどうかを示します。  <br/> |
   
## <a name="remarks"></a>解説

 必要に応じて [Hyperlink.  必要に応じて行に*名前*を付け、わかりやすい名前を行に割り当て、セルの値を設定します。 既存の [Hyperlinks] セクションにハイパーリンクを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
これらのセルを行名で参照できます。これは、シェイプシートウィンドウに赤いテキストで表示されます。 ハイパーリンクにわかりやすい名前を割り当てることができます。 [*名前*] 行をクリックしてから、「 *marketing* 」などの名前を入力します。たとえば、「行名」というハイパーリンクを作成します。 その後、[説明] セルを参照するには、Hyperlink を使用します。説明。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

