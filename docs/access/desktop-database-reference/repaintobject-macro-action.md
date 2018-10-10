---
title: "'RepaintObject/オブジェクトの再描画' マクロ アクション"
TOCTitle: RepaintObject Macro Action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4371ce5482b775ad9c022eeda8202c4b2e0f800d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478129"
---
# <a name="repaintobject-macro-action"></a>"RepaintObject/オブジェクトの再描画" マクロ アクション


**適用されます**Access 2013 |。Office 2013

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
> <UL>
> <LI>
> <P>この動作は、オブジェクトの基になるテーブルまたはクエリからレコードの追加、変更、削除は反映されませんので、データベースの再クエリを発生しません。 オブジェクトまたはそのコントロールのいずれかのソースを再クエリ<STRONG>再クエリ</STRONG>アクションを使用します。 最新のレコードを表示し、適用されたフィルターを削除するには、<STRONG>解除</STRONG>を使用します。</P>
> <LI>
> <P><STRONG>RepaintObject</STRONG>アクション [<STRONG>ホーム</STRONG>] タブ、フォームやデータシートの現在表示されているレコードにするか、他のユーザーが行った変更をすべてを表示する [<STRONG>レコード</STRONG>] グループで [<STRONG>更新</STRONG>] をクリックと同じ効果がありません。</P></LI></UL>



**RepaintObject**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**RepaintObject**メソッドを使用します。

