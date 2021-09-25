---
title: 'HelloData: 簡単な ADO アプリケーション'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63c26ea16f3c93094a877ffb4b9a394b0be89be6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602480"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: 簡単な ADO アプリケーション

**適用先**: Access 2013、Office 2013

ADO ライブラリ検索の例として、"HelloData" という単純な ADO アプリケーションを取り上げます。HelloData では、4 つの主な ADO 操作 (データの取得、検査、編集、および更新) のそれぞれを行います。ADO の基本事項に焦点を当て、コードが複雑になりすぎるのを防ぐために、この例ではエラー処理を最小限に押さえています。

アプリケーションのクエリには、Microsoft SQL Server 2000 に搭載されている Northwind サンプル データベースを使用しています。

**HelloData を実行するには**

1.  ADO 2.5 ライブラリを参照する Visual Basic の標準的な実行可能ファイルのプロジェクトを新規作成します。

2.  フォームの最上部にコマンド ボタンを 4 つ作成し、 **Name** および **Caption** プロパティを以下の表の値に設定します。

3.  ボタンの下に Microsoft **DataGrid コントロール** (Msdatgrd.ocx) を追加します。 Msdatgrd.ocx ファイルには、Visual Basicが付属し \\ 、windows \\ system32 または \\ winnt \\ system32 ディレクトリにあります。 DataGrid コントロールを [ツールボックス] ウィンドウにVisual Basicするには、[コンポーネント **]を** 選択します。次のメニュー **Project** します。 次に、[Microsoft DataGrid Control 6.0 (SP3) (OLEDB)] の横にあるボックスをオンにして **、[OK] をクリックします**。 コントロールをプロジェクトに追加するには、[ツールボックス] から [データ グリッド] コントロールをフォームVisual Basicします。

4.  グリッドの下のフォームに **TextBox** を作成し、プロパティを以下の表の値に設定します。作業が終了すると、フォームは次の図のようになります。

5.  最後に [、HelloData Code](hellodata-code.md) に記載されているコードをコピーし、フォームのコード エディター ウィンドウに貼り付けます。 **F5** キーを押してコードを実行します。

> [!NOTE]
> [!メモ] 次の例およびこのガイドでは、サーバーでの認証用ユーザー ID は "MyId"、パスワードは "123aBc" を使用します。これらの値は、お使いになるサーバーに合わせて有効なログオン認証に置き換えてください。また、"MyServer" も使用するサーバー名に置き換えてください。

コードの詳細については、「HelloData Details」 [を参照してください](hellodata-details.md)。

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
<td><p>フォーム</p></td>
<td><p>名前</p></td>
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
<td><p>名前</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>TextBox</p></td>
<td><p>名前</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>マルチライン</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Command Button</p></td>
<td><p>名前</p></td>
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
<td><p>名前</p></td>
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
<td><p>名前</p></td>
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
<td><p>名前</p></td>
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



