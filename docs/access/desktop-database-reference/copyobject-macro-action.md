---
title: CopyObject マクロ アクション
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a226cca2c37a6e404275c246f2e506b500a58d2b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919627"
---
# <a name="copyobject-macro-action"></a>CopyObject マクロ アクション


**適用されます**Access 2013、Office 2013。

**CopyObject** アクションは、指定したデータベース オブジェクトを別の Access データベースにコピーするか、または同じデータベースや Access プロジェクトに新しい名前でコピーするために使用します。たとえば、既存のオブジェクトを別のデータベースにコピーして使ったり、バックアップ コピーとして保存したりできます。また、多少の変更を加えて類似したオブジェクトを手早く作成することができます。


> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。



## <a name="setting"></a>設定

**CopyObject** アクションの引数は次のとおりです。

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
<td><p><strong>Destination Database/コピー先データベース</strong></p></td>
<td><p>コピー先データベースのパスとファイル名を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>コピー先データベース</strong>] ボックスに、パスとファイル名を入力します。この引数を指定しない場合は、カレント データベースにコピーされます。  </p>

> [!NOTE]
> この引数は、Access データベース環境でのみ使用できます。Access プロジェクト (.adp) 環境でこのアクションを使用する場合は、"Destination Database/コピー先データベース" 引数を指定しないでください。


<p>

					ライブラリ データベースで <strong>CopyObject</strong> アクションが定義されたマクロを実行する場合、この引数が指定されていなければ、Microsoft Office Access 2007 では、オブジェクトがそのライブラリ データベースにコピーされます。

</p></td>
</tr>
<tr class="even">
<td><p><strong>New Name/新しい名前</strong></p></td>
<td><p>オブジェクトの新しい名前を指定します。別のデータベースにコピーする場合は、この引数が指定されていなければ、元のオブジェクトと同じ名前でコピーされます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source Object Type/ソース オブジェクトの種類</strong></p></td>
<td><p>コピーするオブジェクトの種類を指定します。[ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。ナビゲーション ウィンドウで選択したオブジェクトをコピーする場合は、この引数を指定しません。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Source Object Name/ソース オブジェクト名</strong></p></td>
<td><p>コピーするオブジェクトの名前を指定します。[ <strong>ソース オブジェクト名</strong>] ボックスには、データベースのオブジェクトのうち、 <strong>Source Object Type/ソース オブジェクトの種類</strong> 引数で選択された種類のオブジェクトがすべて表示されます。[ <strong>ソース オブジェクト名</strong>] ボックスで、コピーするオブジェクトをクリックします。 <strong>Source Object Type/ソース オブジェクトの種類</strong> 引数を指定しない場合は、この引数も指定しないでください。ライブラリ データベースで <strong>CopyObject</strong> アクションが定義されたマクロを実行する場合は、まずライブラリ データベースでこの名前のオブジェクトが検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**Destination Database/コピー先データベース** 引数と **New Name/新しい名前** 引数の少なくとも一方には必ず値を入力する必要があります。

**Source Object Type/ソース オブジェクトの種類** 引数と **Source Object Name/ソース オブジェクト名** 引数を指定しないと、ナビゲーション ウィンドウで選択したオブジェクトがコピーされます。ナビゲーション ウィンドウでオブジェクトを選択するには、 **SelectObject** アクションの "In Navigation Pane/ナビゲーション ウィンドウから" 引数を [ **はい** ] に設定します。

**CopyObject** アクションの動作は、次の手順を手動で実行した場合と同じです。

1.  ナビゲーション ウィンドウでオブジェクトを選択します。

2.  [ Home] タブの [ Clipboard] グループで [ Copy] をクリックします。

3.  同じタブの [ **貼り付け**] をクリックします。[ **貼り付け**] ダイアログ ボックスが表示され、オブジェクトに新しい名前を付けることができます。 **CopyObject** アクションでは、上記の手順すべてが自動的に実行されます。


> [!NOTE]
> [!メモ] **CopyObject** アクションでデータ アクセス ページをコピーすると、関連付けられた .htm ファイルへのリンクのみがコピーされ、ファイル自体はコピーされません。



マクロの **CopyObject** アクションを実行するには、コピー先データベースのパスとファイル名が実在している必要があります。実在しない場合は、エラー メッセージが表示されます。

Visual Basic for Applications (VBA) モジュールで **CopyObject** アクションを実行するには、 **DoCmd** オブジェクトの **CopyObject** メソッドを使用します。

[ **ファイル**] タブをクリックして、[ **名前を付けて保存**] をクリックすると、ナビゲーション ウィンドウで選択したオブジェクトや現在開いているオブジェクトを手動でコピーできます。このコマンドによってコピーが作成されるのは、カレント データベースのオブジェクトのみです。[ **名前を付けて保存**] ダイアログ ボックスで、コピーに付ける名前を入力し、保存する際のオブジェクトの種類を選択します。元のオブジェクトが既に保存されている場合に、同じオブジェクトをカレント データベースに新しい名前で保存すると、元のバージョンは古い名前でそのまま残ります。

オブジェクトを別の Access データベースに手動でコピーするには、次の操作を行います。

1.  [ **外部データ**] タブの [ **エクスポート**] で [ **その他**] をクリックし、[ **Access データベース**] をクリックします。

2.  [ **エクスポート - Access データベース**] ダイアログ ボックスで、コピー先のデータベースのファイル名を入力します。または[ **参照**] をクリックして [ **名前を付けて保存**] ダイアログ ボックスを表示し、コピー先データベースの場所を指定して、[ **保存**] をクリックします。

3.  [ **エクスポート - Access データベース**] ダイアログ ボックスで、[ **OK**] をクリックします。[ **エクスポート**] ダイアログ ボックスが表示されます。

4.  [ **エクスポート**] ダイアログ ボックスで、コピー先のデータベースでのオブジェクトの名前を入力します。[ **テーブル構造とデータ**] や [ **テーブル構造のみ**] など、テーブルに適用できるオプションを選択します。完了したら、[ **OK**] をクリックします。

