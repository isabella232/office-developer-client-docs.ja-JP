---
title: Database オブジェクト (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ca0538f07f25ffe41288d15fd3737e08eb58f491
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886754"
---
# <a name="database-object-dao"></a>Database オブジェクト (DAO)

**適用されます**Access 2013、Office 2013。

**Database** オブジェクトは、開いているデータベースを表します。

## <a name="remarks"></a>解説

開いているデータベースを操作するには、 **Database** オブジェクトとそのメソッドおよびプロパティを使用します。あらゆる種類のデータベースで、以下の操作を実行できます。

  - **Execute** メソッドを使用して、アクション クエリを実行します。

  - **Connect** プロパティを設定して、ODBC データ ソースへの接続を確立します。

  - **QueryTimeout** プロパティを設定して、ODBC データ ソースに対して実行するクエリを待機する時間を制限します。

  - **RecordsAffected** プロパティを使用して、アクション クエリによって変更されたレコードの数を確認します。

  - **OpenRecordset** メソッドを使用して、選択クエリを実行し、 **Recordset** オブジェクトを作成します。

  - **Version** プロパティを使用して、データベースを作成したデータベース エンジンのバージョンを確認します。

Microsoft Access データベース エンジン データベースを使用すると、Database オブジェクトのテーブル、クエリ、およびリレーションシップに関する情報を作成、変更、または取得するだけでなく、他のメソッド、プロパティ、およびコレクションを使用して **Database** オブジェクトを操作することもできます。たとえば、以下の操作を実行できます。

  - **CreateTableDef** メソッドを使用してテーブルを作成し、 **CreateRelation** メソッドを使用してリレーションを作成します。

  - **CreateProperty** メソッドを使用して、新しい **Database** プロパティを定義します。

  - **CreateQueryDef** メソッドを使用して、持続的または一時的なクエリ定義を作成します。

  - **MakeReplica** 、 **Synchronize** 、および **PopulatePartial** の各メソッドを使用して、データベースのフルまたは部分レプリカを作成して同期します。

  - **CollatingOrder** プロパティを設定して、異なる言語の文字ベース フィールドに五十音順の並べ替え順序を設定します。

**CreateDatabase** メソッドを使用して、 **Databases** コレクションに自動的に追加される永続的な **Database** オブジェクトを作成し、ディスクに保存します。

**OpenDatabase** メソッドを使用する場合、 **DBEngine** オブジェクトを指定する必要はありません。

リンク テーブルを使用するデータベースを開いても、指定した外部ファイルへのリンクは自動的に確立されません。テーブルの **TableDef** オブジェクトまたは **Field** オブジェクトを参照するか、 **Recordset** オブジェクトを開く必要があります。これらのテーブルへのリンクを設定できない場合、トラップ可能なエラーが発生します。データベースにアクセスする権限が必要な場合も、別のユーザーがデータベースを排他的に開いている可能性もあります。このような場合、トラップ可能なエラーが発生します。

**Database** オブジェクトを宣言するプロシージャが実行されると、開いているすべての **Recordset** オブジェクトと共にローカルの **Database** オブジェクトが閉じられます。保留中の更新は失われ、保留中のトランザクションはロールバックされますが、トラップ可能なエラーは発生しません。 **Recordset** オブジェクト変数および **Database** オブジェクト変数をローカルに宣言するプロシージャを終了する前に、保留中のトランザクションまたは編集を明示的に完了し、これらのオブジェクトを閉じる必要があります。

**Workspace** オブジェクトでトランザクション メソッド (**BeginTrans**、**CommitTrans**、または **Rollback**) のいずれかを使用する場合、これらのトランザクションは、**Database** オブジェクトを開いた **Workspace** オブジェクトに対して開かれるすべてのデータベースに適用されます。個別のトランザクションを使用するには、追加の **Workspace** オブジェクトを開いてから、その **Workspace** オブジェクト内でもう 1 つ **Database** オブジェクトを開く必要があります。


> [!NOTE]
> [!メモ] **Databases** コレクションに重複する名前を作成して同じデータ ソースまたはデータベースを複数回開くことができます。 **Database** オブジェクトをオブジェクト変数に割り当てて変数名で参照する必要があります。



## <a name="example"></a>例

この例では、新しい **Database** オブジェクトを作成し、既定の **Workspace** オブジェクト内にある既存の **Database** オブジェクトを開きます。次に、 **Databases** コレクションおよび各 **Database** オブジェクトの **Properties** コレクションを列挙します。

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

この例では、 **CreateDatabase** メソッドを使用して、暗号化された新しい **Database** オブジェクトを作成します。

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
