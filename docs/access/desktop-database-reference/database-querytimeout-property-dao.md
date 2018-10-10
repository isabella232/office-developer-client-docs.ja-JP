---
title: Database.QueryTimeout プロパティ (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 247109d4f71fe153b639c9efa0e6944fb09448b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478443"
---
# <a name="databasequerytimeout-property-dao"></a><span data-ttu-id="64269-102">Database.QueryTimeout プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="64269-102">Database.QueryTimeout Property (DAO)</span></span>


<span data-ttu-id="64269-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="64269-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="64269-104">ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="64269-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="64269-105">構文</span><span class="sxs-lookup"><span data-stu-id="64269-105">Syntax</span></span>

<span data-ttu-id="64269-106">*式*です。QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="64269-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="64269-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="64269-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64269-108">注釈</span><span class="sxs-lookup"><span data-stu-id="64269-108">Remarks</span></span>

<span data-ttu-id="64269-109">既定値は 60 です。</span><span class="sxs-lookup"><span data-stu-id="64269-109">The default value is 60.</span></span>

<span data-ttu-id="64269-p101">Microsoft SQL Server などの ODBC データベースを使用している場合、ネットワーク トラフィックや ODBC サーバーに対する負荷の増大のために、応答が遅れることがあります。無限に待機せずに、待機する時間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="64269-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="64269-p102">[**Connection**](connection-object-dao.md) オブジェクトまたは [**Database**](database-object-dao.md) オブジェクトと共に **QueryTimeout** を使用すると、データベースに関連付けられたすべてのクエリに対してグローバル値が指定されます。特定の [**QueryDef**](querydef-object-dao.md) オブジェクトの **ODBCTimeout** プロパティを設定すると、特定のクエリのこの値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="64269-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="example"></a><span data-ttu-id="64269-114">例</span><span class="sxs-lookup"><span data-stu-id="64269-114">Example</span></span>

<span data-ttu-id="64269-115">この例では、 **ODBCTimeout** プロパティおよび **QueryTimeout** プロパティを使用して、 **Database** オブジェクトの **QueryTimeout** プロパティで、 **Database** オブジェクトから作成された **QueryDef** オブジェクトの **ODBCTimeout** プロパティの既定値を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="64269-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

