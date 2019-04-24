---
title: RepaintObject マクロ アクション
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2ef6c5f38064ae3253cd7e0e58732f63294ceb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306686"
---
# <a name="repaintobject-macro-action"></a>RepaintObject マクロ アクション

**適用先:** Access 2013、Office 2013

"RepaintObject/オブジェクトの再描画" アクションを使用すると、表示が更新されていないデータベース オブジェクトを再描画できます。データベース オブジェクトが指定されている場合はそのオブジェクトを再描画し、指定されていない場合はアクティブなデータベース オブジェクトを再描画します。このとき、コントロールの再計算も行われます。

## <a name="setting"></a>Setting

"RepaintObject/オブジェクトの再描画" アクションの引数は次のとおりです。

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
<td><p><strong>Object Type/オブジェクトの種類</strong></p></td>
<td><p>再描画するオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、または [<strong>関数</strong>] をクリックします。この引数を指定しない場合は、アクティブ オブジェクトが選択されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>オブジェクト名</strong></p></td>
<td><p>再描画するオブジェクトの名前を指定します。 [ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のオブジェクトがすべて表示されます。 If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Microsoft Access では、他の保留中のタスクの実行が終わるまで画面は更新されません。このアクションを使うと、指定したオブジェクトのコントロールを即座に再描画できます。このアクションは、次のような場合に使うと効果的です。

- When you use the **SetValue** action to change values in a number of controls. Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.

- 表示しているフォームのすべてのコントロールにデータが確実に表示されるようにする場合。たとえば、フォームを開いた直後は、OLE オブジェクトを含むコントロールのデータが表示されないことがあります。

> [!NOTE]
> - This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query. Use the **Requery** action to requery the source of the object or one of its controls. Use the **ShowAllRecords** action to display the most recent records and remove any applied filters.
> - **RepaintObject**アクションの動作は、[**ホーム**] タブの [**レコード**] グループで [最新の情報に**更新**] をクリックした場合と同じです。これには、フォームおよびデータシートに現在表示されているレコードに対して行った変更やその他のユーザーが表示されます。

Visual Basic for applications (VBA) モジュールで**RepaintObject**アクションを実行するには、 **DoCmd**オブジェクトの**RepaintObject**メソッドを使用します。

