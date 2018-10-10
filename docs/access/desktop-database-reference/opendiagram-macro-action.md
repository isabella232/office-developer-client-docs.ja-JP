---
title: "'OpenDiagram/ダイアグラムを開く' マクロ アクション"
TOCTitle: OpenDiagram Macro Action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 39557bca91a500a5abf0871d5977418bf067d562
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478828"
---
# <a name="opendiagram-macro-action"></a>"OpenDiagram/ダイアグラムを開く" マクロ アクション


**適用されます**Access 2013 |。Office 2013

Access プロジェクトで、デザイン ビューでデータベース ダイアグラムを開く**OpenDiagram**アクションを使用できます。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

**OpenDiagram**アクションには、次の引数があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Diagram Name/ダイアグラム名</strong></p></td>
<td><p>開くデータベース ダイアグラムの名前です。 マクロ ビルダー] ウィンドウの [<strong>ダイアグラム名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベースのすべてのデータベース ダイアグラムを示しています。 この引数は省略できません。 ライブラリ データベースで<strong>OpenDiagram</strong>アクションを含むマクロを実行すると、Microsoft Access は最初にライブラリ データベースで、し、[現在のデータベース内にこの名前のダイアグラムを検索します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

このアクションの動作は、ナビゲーション ウィンドウでデータベース ダイアグラムをダブルクリックした場合や、ナビゲーション ウィンドウでデータベース ダイアグラムを右クリックして [ **デザイン ビュー**] をクリックした場合と同じです。


> [!TIP]
> <P>ナビゲーション ウィンドウからマクロのアクション行にデータベース ダイアグラムをドラッグできます。 <STRONG>OpenDiagram</STRONG>操作デザイン ビューでデータベース ダイアグラムを開くことが自動的に作成します。</P>



**OpenDiagram**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenDiagram**メソッドを使用します。

