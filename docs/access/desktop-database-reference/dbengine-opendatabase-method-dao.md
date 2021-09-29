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
ms.localizationpriority: high
ms.openlocfilehash: 4c639f14a414c5bd32d1790631a6c1e6baaf1288
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597451"
---
# <a name="dbengineopendatabase-method-dao"></a>DBEngine.OpenDatabase メソッド (DAO)

**適用先**: Access 2013、Office 2013

指定されたデータベースを開き、そのデータベースを表す **[Database](database-object-dao.md)** オブジェクトへの参照を返します。

## <a name="syntax"></a>構文

*式* .OpenDatabase(***Name** _, _*_Options_*_, _*_ReadOnly_*_, _*_Connect_**)

*式* **DBEngine** オブジェクトを表す変数です。

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
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>既存の Microsoft Access データベース ファイルの名前、または ODBC データ ソースのデータ ソース名 (DSN)。この値の設定方法の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>「解説」に記載されたデータベースのさまざまなオプションを設定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> に設定すると、データベースが読み取り専用アクセスで開かれ、<strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>パスワードなどさまざまな接続情報を指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Database

## <a name="remarks"></a>注釈

オプションの引数に使用できる値は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Setting</p></th>
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

dbname を使用する際に一部の注意事項が適用されます。

- 別のユーザーによって既に排他的に開かれているデータベースを指定すると、エラーが発生します。

- 既存のデータベース、または有効な ODBC データ ソース名を指定していない場合は、エラーが発生します。

- この引数で長さ 0 の文字列 ("") を指定し、*connect* で "ODBC;" を指定した場合は、すべての登録済みの ODBC データ ソース名を一覧表示したダイアログ ボックスが表示され、ユーザーがデータベースを選択できるようになります。

データベースを閉じ、その **Database** オブジェクトを **Databases** コレクションから削除するには、そのオブジェクトの **[Close](connection-close-method-dao.md)** メソッドを使用します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンに接続している ODBC データ ソースにアクセスするときは、ODBC データ ソースに接続された **Database** オブジェクトを開いた方が、個々の [TableDef](tabledef-object-dao.md) オブジェクトを ODBC データ ソースの特定のテーブルにリンクさせるよりもアプリケーションのパフォーマンスが向上します。


