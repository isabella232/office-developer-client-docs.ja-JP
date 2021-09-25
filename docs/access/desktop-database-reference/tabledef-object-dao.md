---
title: TableDef オブジェクト (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 90f44c1b8d23ea7e9ae265cfa59fb2dcad3cd1c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605835"
---
# <a name="tabledef-object-dao"></a>TableDef オブジェクト (DAO)

**適用先:** Access 2013、Office 2013

**TableDef** オブジェクトは、ベース テーブルまたはリンク テーブルの保存済み定義を表します (Microsoft Access ワークスペースのみ)。

## <a name="remarks"></a>解説

**TableDef** オブジェクトと、そのメソッドおよびプロパティを使用して、テーブル定義を操作できます。たとえば、以下の操作を実行できます。

- データベースの任意のローカル テーブル、リンク テーブル、または外部キー側のテーブルのフィールドおよびインデックス構造を調べます。

- **Connect** プロパティおよび **SourceTableName** プロパティを使用して、リンク テーブルに関する情報を設定または取得し、 **RefreshLink** メソッドを使用して、リンク テーブルへの接続を更新します。

- **ValidationRule** プロパティおよび **ValidationText** プロパティを使用して、検証条件を設定したり、返したりします。

- **OpenRecordset** メソッドを使用して、テーブル定義に基づいて、テーブル、ダイナセット、ダイナミック、スナップショット、転送専用の種類の **Recordset** オブジェクトを作成します。

ベース テーブルの場合、**RecordCount** プロパティには、指定したデータベース テーブルのレコード数が含まれます。リンク テーブルの場合、**RecordCount** プロパティ設定は常に -1 です。

新しい **TableDef** オブジェクトを作成するには、**[CreateTableDef](database-createtabledef-method-dao.md)** メソッドを使用します。

### <a name="to-add-a-field-to-a-table"></a>テーブルにフィールドを追加するには

1.  テーブルに基づいた **[Recordset](recordset-object-dao.md)** オブジェクトがすべて閉じていることを確認します。

2.  **CreateField** メソッドを使用して、 **Field** オブジェクト変数を作成し、そのプロパティを設定します。

3.  **Append** メソッドを使用して、 **Field** オブジェクトを **TableDef** オブジェクトの **Fields** コレクションに追加します。

インデックスが割り当てられていない場合、 **TableDefs** コレクションから **Field** オブジェクトを削除できますが、フィールドのデータが失われます。

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a>データベースの新しいレコードを格納するテーブルを作成するには

1.  **CreateTableDef** メソッドを使用して、 **TableDef** オブジェクトを作成します。

2.  そのプロパティを設定します。

3.  テーブルのフィールドごとに、 **CreateField** メソッドを使用して、 **Field** オブジェクト変数を作成し、そのプロパティを設定します。

4.  **Append** メソッドを使用して、フィールドを **TableDef** オブジェクトの **Fields** コレクションに追加します。

5.  **Append** メソッドを使用して、新しい **TableDef** オブジェクトを **Database** オブジェクトの **TableDefs** コレクションに追加します。

リンク テーブルは、 **TableDef** オブジェクトの **SourceTableName** プロパティおよび **Connect** プロパティによってデータベースに接続されます。

### <a name="to-link-a-table-to-a-database"></a>テーブルをデータベースにリンクするには

1.  **CreateTableDef** メソッドを使用して、 **TableDef** オブジェクトを作成します。

2.  その **Connect** プロパティおよび **SourceTableName** プロパティ、さらにオプションで **Attributes** プロパティを設定します。

3.  **Append** メソッドを使用して、 **Database** の **TableDefs** コレクションに追加します。

コレクション内の **TableDef** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

**TableDefs**(0)

**TableDefs**("name")

**TableDefs**\!\[name\]

## <a name="example"></a>例

この例では、新しい **TableDef** オブジェクトを作成し、Northwind Database オブジェクトの **TableDefs** コレクションに追加します。次に、 **TableDefs** コレクションおよび新しい **TableDef** オブジェクトの **Properties** コレクションを列挙します。

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

この例では、Northwind データベースで新しい **TableDef** オブジェクトを作成します。

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

次の例は、集計フィールドを作成する方法を示します。 CreateField メソッドで、" **FullName**" という名前のフィールドを作成します。次に、 Expression プロパティを、フィールドの値を計算する式に設定します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
