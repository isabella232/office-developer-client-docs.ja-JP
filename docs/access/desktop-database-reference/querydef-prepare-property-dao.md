---
title: QueryDef.Prepare プロパティ (DAO)
TOCTitle: Prepare Property
ms:assetid: d5a285c4-bd00-028b-b785-f1890db29bab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835035(v=office.15)
ms:contentKeyID: 48547968
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101187
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: fa4d794ce0cd75cf373d7e56e6aec9de3361315c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568629"
---
# <a name="querydefprepare-property-dao"></a>QueryDef.Prepare プロパティ (DAO)

**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .準備

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Prepare** プロパティを使用すると、クエリから一時的なストアド プロシージャをサーバーに作成した後でそのプロシージャを実行するか、またはクエリを直接実行するかを指定できます。既定では、 **Prepare** プロパティは **dbQPrepare** に設定されています。一方、このプロパティを **dbQUnprepare** に設定すると、クエリのプロシージャは準備されません。この場合、クエリは **SQLExecDirect** API を使用して実行されます。

ストアド プロシージャを作成すると初期操作の速度は低下する可能性がありますが、それ以降のクエリに対するすべての参照のパフォーマンスが向上します。ただし、一部のクエリは、ストアド プロシージャの形式で実行できません。これらのクエリに対しては、 **Prepare** プロパティを **dbQUnprepare** に設定する必要があります。

Prepare **が** **dbQPrepare** に設定されている場合 **[、Execute](querydef-execute-method-dao.md)** メソッドの options 引数を **dbExecDirect** に設定することで、クエリの実行時に上書きできます。

> [!NOTE]
> [!メモ] ODBC **SQLPrepare** API は、DAO **[SQL](querydef-sql-property-dao.md)** プロパティを設定した直後に呼び出されます。このため、 **dbQUnprepare** オプションを使用してパフォーマンスを向上させる場合は、 **SQL** プロパティを設定する前に **Prepare** プロパティを設定する必要があります。

## <a name="example"></a>例

この例では、 **Prepare** プロパティを使用して、最初に一時的なストアド プロシージャをサーバーに作成するのではなく、クエリを直接実行するように指定します。

```vb 
Sub PrepareX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set qdfTemp = conPubs.CreateQueryDef("") 
 
 With qdfTemp 
 ' Because you will only run this query once, specify 
 ' the ODBC SQLExecDirect API function. If you do 
 ' not set this property before you set the SQL 
 ' property, the ODBC SQLPrepare API function will 
 ' be called anyway which will nullify any 
 ' performance gain. 
 .Prepare = dbQUnprepare 
 .SQL = "UPDATE roysched " & _ 
 "SET royalty = royalty * 2 " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'" 
 .Execute 
 End With 
 
 Debug.Print "Query results:" 
 
 ' Open recordset containing modified records. 
 Set rstTemp = conPubs.OpenRecordset( _ 
 "SELECT * FROM roysched " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'") 
 
 ' Enumerate recordset. 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , !title_id, !lorange, _ 
 !hirange, !royalty 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 conPubs.Close 
 wrkODBC.Close 
 
```

