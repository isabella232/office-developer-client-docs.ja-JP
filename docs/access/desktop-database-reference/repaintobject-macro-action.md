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
ms.openlocfilehash: 69429aa0c623be06eae93a5e62fa06f1f0687007
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996462"
---
# <a name="repaintobject-macro-action"></a>RepaintObject マクロ アクション

**適用されます**Access 2013、Office 2013。

指定されていない場合は、保留中の指定されたデータベース オブジェクトまたはアクティブなデータベース オブジェクトでは、画面の更新を完了する**RepaintObject**アクションを使用できます。 このような更新には、オブジェクトのコントロールの再計算が含まれます。

## <a name="setting"></a>設定値

**RepaintObject**アクションには、次の引数があります。

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
<td><p>再描画するオブジェクトの名前。 [ <strong>オブジェクト名</strong> ] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。 <strong>オブジェクトの型</strong>引数を空白のままにする場合は、この引数を指定しないも。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

Microsoft Access では、他の保留中のタスクの実行が終わるまで画面は更新されません。このアクションを使うと、指定したオブジェクトのコントロールを即座に再描画できます。このアクションは、次のような場合に使うと効果的です。

- いくつかのコントロールの値を変更するのには **、アクション**を使用します。 アクセスの変更をすぐに表示されないことが他のコントロール (演算コントロールなど) が変更されたコントロールの値に依存している場合に特に。

- 表示しているフォームのすべてのコントロールにデータが確実に表示されるようにする場合。たとえば、フォームを開いた直後は、OLE オブジェクトを含むコントロールのデータが表示されないことがあります。

> [!NOTE]
> - この動作は、オブジェクトの基になるテーブルまたはクエリからレコードの追加、変更、削除は反映されませんので、データベースの再クエリを発生しません。 オブジェクトまたはそのコントロールのいずれかのソースを再クエリ**再クエリ**アクションを使用します。 最新のレコードを表示し、適用されたフィルターを削除するには、**解除**を使用します。
> - **RepaintObject**アクション [**ホーム**] タブ、フォームやデータシートの現在表示されているレコードにするか、他のユーザーが行った変更をすべてを表示する [**レコード**] グループで [**更新**] をクリックと同じ効果がありません。

**RepaintObject**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**RepaintObject**メソッドを使用します。

