---
title: QueryDef.ODBCTimeout プロパティ (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ceb3cf0fa2e16af4df23c6511fd6d1421487a409
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922756"
---
# <a name="querydefodbctimeout-property-dao"></a><span data-ttu-id="30305-102">QueryDef.ODBCTimeout プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="30305-102">QueryDef.ODBCTimeout property (DAO)</span></span>


<span data-ttu-id="30305-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="30305-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30305-104">ODBC データベースに対して **[QueryDef](querydef-object-dao.md)** を実行したときに、タイムアウト エラーが発生するまでの待ち時間を秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="30305-104">Indicates the number of seconds to wait before a timeout error occurs when a **[QueryDef](querydef-object-dao.md)** is executed on an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="30305-105">構文</span><span class="sxs-lookup"><span data-stu-id="30305-105">Syntax</span></span>

<span data-ttu-id="30305-106">*式*です。補足</span><span class="sxs-lookup"><span data-stu-id="30305-106">*expression* .ODBCTimeout</span></span>

<span data-ttu-id="30305-107">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="30305-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="30305-108">注釈</span><span class="sxs-lookup"><span data-stu-id="30305-108">Remarks</span></span>

<span data-ttu-id="30305-p101">**ODBCTimeout** プロパティを -1 に設定すると、タイムアウトの既定値は、 [QueryDef](database-querytimeout-property-dao.md) オブジェクトに含まれている [**Connection**](connection-object-dao.md) オブジェクトまたは [**Database**](database-object-dao.md) オブジェクトの \*\*\*\*QueryTimeout\*\*\*\* プロパティに現在設定されている値になります。 **ODBCTimeout** プロパティを 0 に設定すると、タイムアウト エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="30305-p101">When the **ODBCTimeout** property is set to -1, the timeout defaults to the current setting of the **[QueryTimeout](database-querytimeout-property-dao.md)** property of the **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object that contains the **QueryDef**. When the **ODBCTimeout** property is set to 0, no timeout error occurs.</span></span>

<span data-ttu-id="30305-p102">Microsoft SQL Server などの ODBC データベースを使用している場合、ネットワーク トラフィックや ODBC サーバーに対する負荷の増大のために、遅延が発生することがあります。無限に待機しないように、エラーが返されるまでの待ち時間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="30305-p102">When you're using an ODBC database, such as Microsoft SQL Server, delays can occur because of network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait before returning an error.</span></span>

<span data-ttu-id="30305-113">**QueryDef** オブジェクトの **ODBCTimeout** プロパティの設定値は、 **QueryDef** オブジェクトに含まれている **Connection** オブジェクトまたは **Database** オブジェクトの **QueryTimeout** プロパティで指定される値より優先されますが、これはその **QueryDef** オブジェクトに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="30305-113">Setting the **ODBCTimeout** property of a **QueryDef** object overrides the value specified by the **QueryTimeout** property of the **Connection** or **Database** object containing the **QueryDef**, but only for that **QueryDef** object.</span></span>

## <a name="example"></a><span data-ttu-id="30305-114">例</span><span class="sxs-lookup"><span data-stu-id="30305-114">Example</span></span>

<span data-ttu-id="30305-115">この例では、 **ODBCTimeout** プロパティおよび **QueryTimeout** プロパティを使用して、 **Database** オブジェクトの **QueryTimeout** プロパティで、 **Database** オブジェクトから作成された **QueryDef** オブジェクトの **ODBCTimeout** プロパティの既定値を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="30305-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

