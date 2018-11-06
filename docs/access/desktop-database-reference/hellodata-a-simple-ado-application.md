---
title: 'HelloData: 単純な ADO アプリケーション'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 359816f828191a8643941a21ac520ba7b3231e6b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998204"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: 単純な ADO アプリケーション

**適用されます**Access 2013、Office 2013。

ADO ライブラリ検索の例として、"HelloData" という単純な ADO アプリケーションを取り上げます。HelloData では、4 つの主な ADO 操作 (データの取得、検査、編集、および更新) のそれぞれを行います。ADO の基本事項に焦点を当て、コードが複雑になりすぎるのを防ぐために、この例ではエラー処理を最小限に押さえています。

アプリケーションのクエリには、Microsoft SQL Server 2000 に搭載されている Northwind サンプル データベースを使用しています。

**HelloData を実行するには**

1.  ADO 2.5 ライブラリを参照する Visual Basic の標準的な実行可能ファイルのプロジェクトを新規作成します。

2.  フォームの最上部にコマンド ボタンを 4 つ作成し、 **Name** および **Caption** プロパティを以下の表の値に設定します。

3.  ボタンの下には、 **Microsoft データ グリッド コントロール**(Msdatgrd.ocx) を追加します。 Msdatgrd.ocx ファイルは Visual Basic に付属して、ある、 \\windows\\system32 または\\winnt\\system32 ディレクトリ。 Visual Basic の [ツールボックス] ウィンドウには、DataGrid コントロールを追加するには、**プロジェクト**] メニューの [**コンポーネント]** を選択します。 チェック ボックスを横に"Microsoft データ グリッド コントロール 6.0 (SP3) (ole DB)"[ **OK**] をクリックします。 コントロールをプロジェクトに追加するに DataGrid コントロールをツールボックスから Visual Basic フォームにドラッグします。

4.  グリッドの下のフォームに **TextBox** を作成し、プロパティを以下の表の値に設定します。作業が終了すると、フォームは次の図のようになります。

5.  最後に、 [HelloData のコード](hellodata-code.md)に記載されているコードをコピーし、フォームのコード エディター ウィンドウに貼り付けます。 **F5** キーを押してコードを実行します。

> [!NOTE]
> [!メモ] 次の例およびこのガイドでは、サーバーでの認証用ユーザー ID は "MyId"、パスワードは "123aBc" を使用します。これらの値は、お使いになるサーバーに合わせて有効なログオン認証に置き換えてください。また、"MyServer" も使用するサーバー名に置き換えてください。

コードの詳細については、 [HelloData の詳細](hellodata-details.md)を参照してください。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>コントロールの種類</p></th>
<th><p>プロパティ</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Form</p></td>
<td><p>Name</p></td>
<td><p>Form1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Height</p></td>
<td><p>6500</p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p>Width</p></td>
<td><p>6500</p></td>
</tr>
<tr class="even">
<td><p>MS DataGrid</p></td>
<td><p>Name</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>テキスト ボックス</p></td>
<td><p>Name</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Multiline</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Command Button</p></td>
<td><p>Name</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Get Data</p></td>
</tr>
<tr class="odd">
<td><p>Command Button</p></td>
<td><p>Name</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Examine Data</p></td>
</tr>
<tr class="odd">
<td><p>Command Button</p></td>
<td><p>Name</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Edit Data</p></td>
</tr>
<tr class="odd">
<td><p>Command Button</p></td>
<td><p>Name</p></td>
<td><p>cmdUpdateData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Update Data</p></td>
</tr>
</tbody>
</table>



