---
title: Workspace.OpenDatabase メソッド (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ca2ccb4183a59c2b579fd4375f26aa4fd539532f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302584"
---
# <a name="workspaceopendatabase-method-dao"></a>Workspace.OpenDatabase メソッド (DAO)

**適用先:** Access 2013、Office 2013

**[Workspace](workspace-object-dao.md)** オブジェクト内で指定されたデータベースを開き、そのデータベースを表す **[Database](database-object-dao.md)** オブジェクトへの参照を返します。

## <a name="syntax"></a>構文

*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*expression*: **Workspace** オブジェクトを表す変数。

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
<td><p>既存の Microsoft Access データベース エンジンのデータベース ファイル名、または ODBC データ ソースのデータ ソース名 (DSN) です。この値を設定する方法の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティのトピックを参照してください。</p></td>
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

<br/>

データベースを開くと、そのデータベースは自動的に **Databases** コレクションに追加されます。

dbname を使用する際に一部の注意事項が適用されます。

- 別のユーザーによって既に排他的に開かれているデータベースを指定すると、エラーが発生します。

- 既存のデータベース、または有効な ODBC データ ソース名を指定していない場合は、エラーが発生します。

- この引数で長さ 0 の文字列 ("") を指定し、*connect* で "ODBC;" を指定した場合は、すべての登録済みの ODBC データ ソース名を一覧表示したダイアログ ボックスが表示され、ユーザーがデータベースを選択できるようになります。

データベースを閉じ、その **Database** オブジェクトを **Databases** コレクションから削除するには、そのオブジェクトの **[Close](connection-close-method-dao.md)** メソッドを使用します。

> [!NOTE]
> Microsoft Access データベース エンジンに接続している ODBC データ ソースにアクセスするときは、ODBC データ ソースに接続された **Database** オブジェクトを開いた方が、個々の **[TableDef](tabledef-object-dao.md)** オブジェクトを ODBC データ ソースの特定のテーブルにリンクさせるよりもアプリケーションのパフォーマンスが向上します。

## <a name="example"></a>例

この例では、**OpenDatabase** メソッドを使用して、Microsoft Access データベースと、Microsoft Access データベース エンジンに接続された 2 つの ODBC データベースを開きます。

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

