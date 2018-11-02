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
ms.openlocfilehash: f1d587501cb9a3279db055b9eee27d765e002a03
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925941"
---
# <a name="querydefprepare-property-dao"></a><span data-ttu-id="46aa9-102">QueryDef.Prepare プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="46aa9-102">QueryDef.Prepare property (DAO)</span></span>


<span data-ttu-id="46aa9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="46aa9-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="46aa9-104">構文</span><span class="sxs-lookup"><span data-stu-id="46aa9-104">Syntax</span></span>

<span data-ttu-id="46aa9-105">*式*です。準備</span><span class="sxs-lookup"><span data-stu-id="46aa9-105">*expression* .Prepare</span></span>

<span data-ttu-id="46aa9-106">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="46aa9-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="46aa9-107">注釈</span><span class="sxs-lookup"><span data-stu-id="46aa9-107">Remarks</span></span>

<span data-ttu-id="46aa9-p101">**Prepare** プロパティを使用すると、クエリから一時的なストアド プロシージャをサーバーに作成した後でそのプロシージャを実行するか、またはクエリを直接実行するかを指定できます。既定では、 **Prepare** プロパティは **dbQPrepare** に設定されています。一方、このプロパティを **dbQUnprepare** に設定すると、クエリのプロシージャは準備されません。この場合、クエリは **SQLExecDirect** API を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="46aa9-p101">You can use the **Prepare** property to either have the server create a temporary stored procedure from your query and then execute it, or just have the query executed directly. By default the **Prepare** property is set to **dbQPrepare**. However, you can set this property to **dbQUnprepare** to prohibit preparing of the query. In this case, the query is executed using the **SQLExecDirect** API.</span></span>

<span data-ttu-id="46aa9-p102">ストアド プロシージャを作成すると初期操作の速度は低下する可能性がありますが、それ以降のクエリに対するすべての参照のパフォーマンスが向上します。ただし、一部のクエリは、ストアド プロシージャの形式で実行できません。これらのクエリに対しては、 **Prepare** プロパティを **dbQUnprepare** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46aa9-p102">Creating a stored procedure can slow down the initial operation, but increases performance of all subsequent references to the query. However, some queries cannot be executed in the form of stored procedures. In these cases, you must set the **Prepare** property to **dbQUnprepare**.</span></span>

<span data-ttu-id="46aa9-115">**準備**が**dbQPrepare**に設定されているこの**dbExecDirect**に**[Execute](querydef-execute-method-dao.md)** メソッドのオプションの引数を設定することによってクエリが実行されるときは、オーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="46aa9-115">If **Prepare** is set to **dbQPrepare**, this can be overridden when the query is executed by setting the **[Execute](querydef-execute-method-dao.md)** method's options argument to **dbExecDirect**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="46aa9-p103">[!メモ] ODBC <STRONG>SQLPrepare</STRONG> API は、DAO <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> プロパティを設定した直後に呼び出されます。このため、 <STRONG>dbQUnprepare</STRONG> オプションを使用してパフォーマンスを向上させる場合は、 <STRONG>SQL</STRONG> プロパティを設定する前に <STRONG>Prepare</STRONG> プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46aa9-p103">The ODBC <STRONG>SQLPrepare</STRONG> API is called as soon as the DAO <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> property is set. Therefore, if you want to improve performance using the <STRONG>dbQUnprepare</STRONG> option, you must set the <STRONG>Prepare</STRONG> property before setting the <STRONG>SQL</STRONG> property.</span></span></P>



## <a name="example"></a><span data-ttu-id="46aa9-118">例</span><span class="sxs-lookup"><span data-stu-id="46aa9-118">Example</span></span>

<span data-ttu-id="46aa9-119">この例では、 **Prepare** プロパティを使用して、最初に一時的なストアド プロシージャをサーバーに作成するのではなく、クエリを直接実行するように指定します。</span><span class="sxs-lookup"><span data-stu-id="46aa9-119">This example uses the **Prepare** property to specify that a query should be executed directly rather than first creating a temporary stored procedure on the server.</span></span>

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

