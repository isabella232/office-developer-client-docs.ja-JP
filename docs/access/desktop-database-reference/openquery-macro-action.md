---
title: OpenQuery マクロ アクション
TOCTitle: OpenQuery Macro Action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 30d4f245618e305be0e46b75cc0ea5c224444fa8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478308"
---
# <a name="openquery-macro-action"></a>OpenQuery マクロ アクション


**適用されます**Access 2013 |。Office 2013

**OpenQuery** アクションを使用すると、選択クエリまたはクロス集計クエリをデータシート ビュー、デザイン ビュー、印刷プレビューのいずれかで開くことができます。このアクションでは、アクション クエリが実行されます。クエリを開くときのデータ入力モードを選択することもできます。


> [!NOTE]
> <P>[!メモ] このアクションは、Access データベース (.mdb または .accdb) 環境でのみ使用できます。Access プロジェクト (.adp) 環境で使用する場合は、 <STRONG>OpenView</STRONG> アクション、 <STRONG>OpenStoredProcedure</STRONG> アクション、または <STRONG>OpenFunction</STRONG> アクションのトピックを参照してください。</P>



## <a name="setting"></a>設定

**OpenQuery** アクションの引数は次のとおりです。

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
<td><p><strong>Query Name/クエリ名</strong></p></td>
<td><p>開くクエリの名前を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>クエリ名</strong>] ボックスには、カレント データベース内のクエリがすべて表示されます。この引数は省略できません。ライブラリ データベースで <strong>OpenQuery</strong> アクションが定義されているマクロを実行すると、この名前のクエリが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
<tr class="even">
<td><p><strong>View/ビュー</strong></p></td>
<td><p>クエリを開くときのビューを指定します。[ <strong>ビュー</strong>] ボックスで、[ <strong>データシート ビュー</strong>]、[ <strong>デザイン ビュー</strong>]、[ <strong>印刷プレビュー</strong>]、[ <strong>ピボットテーブル ビュー</strong>]、または [ <strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [ <strong>データシート ビュー</strong>] です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode/データ モード</strong></p></td>
<td><p>クエリを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているクエリにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [ <strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [ <strong>編集</strong>]、レコードの表示のみを許可する場合は [ <strong>読み取り専用</strong>] をクリックします。既定値は [ <strong>編集</strong>] です。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**View/ビュー** 引数に [ **データシート ビュー**] を指定すると、選択クエリ、クロス集計クエリ、ユニオン クエリ、または **ReturnsRecords/レコード表示** プロパティが [ **はい** に設定されているパススルー クエリの場合は、クエリの結果セットが表示されます。一方、アクション クエリ、データ定義クエリ、または **ReturnsRecords /レコード表示** プロパティが [ **いいえ** ] に設定されているパススルー クエリの場合は、そのクエリが実行されます。

**OpenQuery** アクションの動作は、ナビゲーション ウィンドウでクエリをダブルクリックした場合や、ナビゲーション ウィンドウでクエリを右クリックしてビューをクリックした場合と同じです。このアクションにより、別のオプションも選択できます。

**Tips/ヒント**

  - クエリをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、クエリをデータシート ビューで開く **OpenQuery** アクションが自動的に作成されます。 クエリが開いているときにデザイン ビューに切り替えると、クエリの **Data Mode/データ モード** 引数の設定は解除されます。再びデータシート ビューに切り替えても、元の設定には戻りません。

  - アクション クエリを実行すると、通常は、それがアクション クエリであること、および影響を受けるレコード数を示すシステム メッセージが表示されますが、これを表示しないようにするには、 **SetWarnings** アクションを使用します。

Visual Basic for Applications (VBA) モジュールで **OpenQuery** アクションを実行するには、 **DoCmd** オブジェクトの **OpenQuery** メソッドを使用します。

