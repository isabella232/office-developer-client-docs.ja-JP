---
title: Requery マクロ アクション
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e59a1f5ce676ceaa1b0b346a38b4487b3233e514
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997379"
---
# <a name="requery-macro-action"></a>Requery マクロ アクション

**適用されます**Access 2013、Office 2013。

**アクション**を使用すると、コントロールのソースを再クエリ アクティブ オブジェクトの指定されたコントロール内のデータを更新します。 コントロールを指定しない場合は、オブジェクト自体のソースを再クエリします。 アクティブ オブジェクトやそのコントロールの表示データを最新のものにするには、このアクションを使います。

## <a name="setting"></a>設定値

**アクション**には、次の引数があります。

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
<td><p><strong>コントロール名</strong></p></td>
<td><p>更新するコントロールの名前。 [マクロ ビルダー] ウィンドウの [<strong>コントロール名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションで、コントロールの名前を入力します。 完全修飾識別子ではなく、コントロールの名前だけを使用する必要があります (<strong>フォーム</strong>!<em>formname</em>!<em>controlname</em>)。 この引数はアクティブ オブジェクトのソースを再クエリするのには空白のままにします。 アクティブ オブジェクトがデータシートまたはクエリの結果のかどうか、設定する必要がありますこの引数を指定しません。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**再クエリ**アクションは、次のいずれかを行います。

- 指定したコントロールやオブジェクトの基になるクエリの再実行。

- コントロールやオブジェクトの基になるテーブルで追加、変更、または削除されたレコードの反映。

> [!NOTE]
> **再クエリ**アクションは、レコード ポインターの位置には影響しません。

クエリやテーブルに基づくコントロールには次のようなものがあります。

- リスト ボックスとコンボ ボックス。

- サブフォーム コントロール。

- グラフなどの OLE オブジェクト。

- **DSum** などの定義域集計関数が含まれるコントロール。

指定されたコントロールがクエリまたはテーブルに基づいていない場合、このアクションによってコントロールの再計算が実行されます。

"Control Name/コントロール名" 引数を指定しない場合、"Requery/再クエリ" アクションの動作は、オブジェクトにフォーカスがあるときに Shift キーを押しながら F9 キーを押した場合と同じです。サブフォーム コントロールにフォーカスがある場合は、そのサブフォームのソースのみが再クエリされます (この動作も、Shift キーを押しながら F9 キーを押した場合と同じです)。

> [!NOTE]
> コントロールやオブジェクトのソースを再**クエリを再実行**します。 対照的に、 **RepaintObject**アクションは、指定したオブジェクト内のコントロールを再描画がしないデータベースの再クエリを実行または新しいレコードを表示します。 **解除**だけでなく、アクティブなオブジェクトを再クエリが、**アクション**の操作を行いますが、適用されたフィルターが削除されます。

アクティブ オブジェクトにないコントロールを再クエリする場合は、**アクション**または**DoCmd**オブジェクトの対応する、 **Requery**メソッドではない、(VBA) モジュールの Visual Basic for Applications の**Requery**メソッドを使用する必要があります。 **Requery**メソッドを VBA では、**アクション**または**DoCmd.Requery**メソッドよりも高速です。 さらに、**アクション**または**DoCmd.Requery**メソッドを使用すると、Microsoft Access クエリを閉じるし、データベースから再読み込みしていますが、アクセスが終了して、再読み込みすることがなくクエリを再度実行、 **Requery**メソッドを使用する場合。 ActiveX データ オブジェクト (ADO) の**Requery**メソッドが、Access の**Requery**メソッドと同じように動作する注意してください。

