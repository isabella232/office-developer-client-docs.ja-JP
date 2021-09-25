---
title: OpenDiagram マクロ アクション
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 5334c23603fbc90dc3736236a60dd256bc50c11c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602102"
---
# <a name="opendiagram-macro-action"></a>OpenDiagram マクロ アクション

**適用先**: Access 2013、Office 2013

In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"OpenDiagram/ダイアグラムを開く" アクションの引数は次のとおりです。

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
<td><p>開くデータベース ダイアグラムの名前を指定します。 [マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>ダイアグラム名</strong>] ボックスには、カレント データベース内のデータベース ダイアグラムがすべて表示されます。 この引数は省略できません。 ライブラリ データベースで "OpenDiagram/ダイアグラムを開く" アクションが定義されているマクロを実行すると、この名前のダイアグラムが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

このアクションの動作は、ナビゲーション ウィンドウでデータベース ダイアグラムをダブルクリックした場合や、ナビゲーション ウィンドウでデータベース ダイアグラムを右クリックして [**デザイン ビュー**] をクリックした場合と同じです。

> [!TIP]
> You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.

To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.

