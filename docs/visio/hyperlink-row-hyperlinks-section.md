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
description: 図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
ms.openlocfilehash: 36b9b62f248e4f5b9407156a79fa674dc2e8f14d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390255"
---
# <a name="hyperlink-row-hyperlinks-section"></a>[Hyperlink] 行 ([ハイパーリンク] セクション)

図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
  
ハイパーリンク行の名前はハイパーリンクです。 *名*と、次のセルが含まれています。 詳細については、特定のセルを参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[説明](description-cell-hyperlinks-section.md) <br/> |ハイパーリンクを説明するテキスト文字列です。  <br/> |
|[住所](address-cell-hyperlinks-section.md) <br/> |移動先の URL アドレス、MS-DOS ファイル名、または UNC パスです。  <br/> |
|[サブアドレス](subaddress-cell-hyperlinks-section.md) <br/> |リンク先のターゲット図面内での位置です。  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |URL の解決に使用される情報を渡す文字列です。  <br/> |
|[フレーム](frame-cell-hyperlinks-section.md) <br/> |ActiveX コンテナーで、ActiveX の図面として Microsoft Office Visio の図面を開く場合に、ターゲットとするフレームの名前です。既定では、空の文字列です。  <br/> |
|[[Sortkey]](sortkey-cell-hyperlinks-section.md) <br/> |ハイパーリンクがショートカット メニューに表示されるときの順序を判別します。  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |ハイパーリンクを新しいウィンドウで開くかどうかを指定します。 TRUE の場合、リンク先のページ、ドキュメント、または web サイトを新しいウィンドウで開きます。 既定値は、FALSE です。  <br/> |
|[Default](default-cell-hyperlinks-section.md) <br/> |図形またはページに対する既定のハイパーリンクです。  <br/> |
|[非表示](invisible-cell-hyperlinks-section.md) <br/> |ハイパーリンクがショートカット メニューに表示されるかどうかを示します。  <br/> |
   
## <a name="remarks"></a>備考

 多くのハイパーリンクを追加できます。  *名前*の行、行に意味のある名前を割り当てるし、セルの値を設定します。 既存の [Hyperlinks] セクションにハイパーリンクを追加するには、行を右クリックし、ショートカット メニューの [**行の挿入**] をクリックします。 
  
行名を赤いテキストで、[シェイプ シート] ウィンドウに表示されるが、これらのセルを参照できます。 ハイパーリンクにわかりやすい名前を割り当てます。 *名*の行は、行をクリックし、Hyperlink.Marketing 行の名前を作成するたとえば、*マーケティング*などの名前を入力します。 割り当てる説明] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

