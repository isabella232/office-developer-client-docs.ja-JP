---
title: TableDef.RefreshLink メソッド (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3092a623dc84726c4f2d217c0eaea40546b48627
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631696"
---
# <a name="tabledefrefreshlink-method-dao"></a>TableDef.RefreshLink メソッド (DAO)

**適用先**: Access 2013、Office 2013
 
リンク テーブルの接続情報を更新します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .RefreshLink

*式***TableDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

リンク テーブルの接続情報を変更するには、対応する **[TableDef](connection-connect-property-dao.md)** オブジェクトの Connect プロパティをリセットしてから **、RefreshLink** メソッドを使用して情報を更新します。  **RefreshLink メソッドを** 使用しても、リンクテーブルのプロパティと Relation オブジェクトは **[変更](relation-object-dao.md)** されません。

リンク テーブルを表す **TableDef** オブジェクトに関連付けられたすべてのコレクションにこの接続情報を反映するには、各コレクションで **[Refresh](tabledefs-refresh-method-dao.md)** メソッドを使用する必要があります。

## <a name="example"></a>例

この例では、 **RefreshLink** メソッドを使用して、リンク テーブルの接続が、あるデータ ソースから別のデータ ソースに変更された後に、リンク テーブルのデータを更新します。このプロシージャを実行するには、RefreshLinkOutput プロシージャが必要です。

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

