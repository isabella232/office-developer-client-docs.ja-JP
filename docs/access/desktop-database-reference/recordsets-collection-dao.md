---
title: Recordsets コレクション (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309304"
---
# <a name="recordsets-collection-dao"></a>Recordsets コレクション (DAO)

**適用先:** Access 2013、Office 2013

**Recordsets** コレクションには、 **Connection** または **Database** オブジェクト内のすべての開いている **Recordset** オブジェクトが含まれます。

## <a name="remarks"></a>注釈

DAO オブジェクトを使用する場合は、 **Recordset** オブジェクトを使用してほぼすべてのデータを操作します。

新しい **Recordset** オブジェクトは、 **Recordset** オブジェクトを開いたときに **Recordsets** コレクションに自動的に追加され、オブジェクトを閉じたときに自動的に削除されます。

**Recordset** オブジェクト変数は必要な数だけ作成できます。異なる **Recordset** オブジェクトでも、競合せずに同じテーブル、クエリ、およびフィールドにアクセスできます。

コレクション内の **Recordset** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- **Recordsets**(0)

- **Recordsets**("name")

- **レコードセット**\!\[名\]

> [!NOTE]
> [!メモ] 同じデータ ソースまたはデータベースから **Recordset** オブジェクトを複数回開いて、 **Recordsets** コレクションに重複する名前を作成できます。 **Recordset** オブジェクトをオブジェクト変数に割り当て、変数名で参照する必要があります。

## <a name="example"></a>例

次の使用例は、4 種類の **Recordset** オブジェクトを開き、現在の **Recordsets** オブジェクトの Recordsets コレクションを列挙して、各 **Recordsets** オブジェクトの **Database** コレクションを列挙することで、 **Properties** オブジェクトおよび **Recordset** コレクションを示します。

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
