---
title: DBEngine.OpenDatabase メソッド (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a00c61ce4cbb9cb9d6088d521f0c2bdb3cf7f573
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998076"
---
# <a name="dbengineopendatabase-method-dao"></a>DBEngine.OpenDatabase メソッド (DAO)

**適用されます**Access 2013、Office 2013。

指定されたデータベースを開き、そのデータベースを表す **[Database](database-object-dao.md)** オブジェクトへの参照を取得します。

## <a name="syntax"></a>構文

*式*です。OpenDatabase (***名前***、***オプション***、***読み取り専用***、***接続***)

*式***DBEngine**オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>既存の Microsoft Access データベース ファイルの名前、または ODBC データ ソースのデータ ソース名 (DSN)。この値の設定方法の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>「備考」に記載されたデータベースのさまざまなオプションを設定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p><strong>True</strong> に設定すると、データベースが読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>パスワードなどさまざまな接続情報を指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

データベース

## <a name="remarks"></a>注釈

引数 options で使用できる値は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>設定</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>データベースを排他モードで開きます。</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(既定値) データベースを共有モードで開きます。</p></td>
</tr>
</tbody>
</table>


データベースを開くと、そのデータベースは自動的に **Databases** コレクションに追加されます。

データベース名を使用する場合は、いくつかの考慮事項が適用されます。

- 別のユーザーによって既に排他的に開かれているデータベースを指定すると、エラーが発生します。

- 既存のデータベース、または有効な ODBC データ ソース名を指定していない場合は、エラーが発生します。

- 長さ 0 の文字列である場合 ("") とは、"ODBC;"は、*接続*ユーザーがデータベースを選択できるように登録されているすべての ODBC データ ソース名をリストするダイアログ ボックスが表示されます。

データベースを閉じ、その **Database** オブジェクトを **Databases** コレクションから削除するには、そのオブジェクトの **[Close](connection-close-method-dao.md)** メソッドを使用します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンに接続している ODBC データ ソースにアクセスするときは、ODBC データ ソースに接続された **Database** オブジェクトを開いた方が、個々の [TableDef](tabledef-object-dao.md) オブジェクトを ODBC データ ソースの特定のテーブルにリンクさせるよりもアプリケーションのパフォーマンスが向上します。


