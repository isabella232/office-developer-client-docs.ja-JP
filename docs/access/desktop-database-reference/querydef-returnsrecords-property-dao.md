---
title: QueryDef.ReturnsRecords プロパティ (DAO)
TOCTitle: ReturnsRecords Property
ms:assetid: 3d1e538b-4d60-588f-4a20-89f1e2b434e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192701(v=office.15)
ms:contentKeyID: 48544334
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053005
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f1d10a8e348021d88510519c61825714ca434b3b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477994"
---
# <a name="querydefreturnsrecords-property-dao"></a><span data-ttu-id="5d9b8-102">QueryDef.ReturnsRecords プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d9b8-102">QueryDef.ReturnsRecords Property (DAO)</span></span>


<span data-ttu-id="5d9b8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d9b8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="5d9b8-104">外部データベースに対する SQL パススルー クエリでレコードを返すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5d9b8-104">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d9b8-105">構文</span><span class="sxs-lookup"><span data-stu-id="5d9b8-105">Syntax</span></span>

<span data-ttu-id="5d9b8-106">*式*です。ReturnsRecords</span><span class="sxs-lookup"><span data-stu-id="5d9b8-106">*expression* .ReturnsRecords</span></span>

<span data-ttu-id="5d9b8-107">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="5d9b8-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d9b8-108">注釈</span><span class="sxs-lookup"><span data-stu-id="5d9b8-108">Remarks</span></span>

<span data-ttu-id="5d9b8-p101">外部データベースに対するすべての SQL パススルー クエリで、レコードが返されるわけではありません。たとえば、SQL UPDATE ステートメントでは、レコードを返さずにレコードを更新しますが、SQL SELECT ステートメントではレコードを返します。クエリでレコードが返される場合、 **ReturnsRecords** プロパティは **True** に設定されます。クエリでレコードが返されない場合、 **ReturnsRecords** プロパティは **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b8-p101">Not all SQL pass-through queries to external databases return records. For example, an SQL UPDATE statement updates records without returning records, while an SQL SELECT statement does return records. If the query returns records, set the **ReturnsRecords** property to **True**; if the query doesn't return records, set the **ReturnsRecords** property to **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5d9b8-112">[!メモ] <A href="querydef-connect-property-dao.md">ReturnsRecords</A> プロパティを設定する前に、 <STRONG><STRONG>Connect</STRONG></STRONG> プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d9b8-112">You must set the <STRONG><A href="querydef-connect-property-dao.md">Connect</A></STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>



## <a name="example"></a><span data-ttu-id="5d9b8-113">例</span><span class="sxs-lookup"><span data-stu-id="5d9b8-113">Example</span></span>

<span data-ttu-id="5d9b8-p102">この例では、 **Connect** プロパティと **ReturnsRecords** プロパティを使用して、Microsoft SQL Server データベースから本年度の現在までの売り上げ金額に基づいて上位 5 冊の本の題名を選択します。売り上げ金額がまったく同じ場合、クエリの結果を表示するリストのサイズを拡張して、その理由を説明するメッセージを印刷します。</span><span class="sxs-lookup"><span data-stu-id="5d9b8-p102">This example uses the **Connect** and **ReturnsRecords** properties to select the top five book titles from a Microsoft SQL Server database based on year-to-date sales amounts. In the event of an exact match in sales amounts, the example increases the size of the list displaying the results of the query and prints a message explaining why this occurred.</span></span>

```vb 
Sub ClientServerX1() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTopFive As Recordset 
 Dim strMessage As String 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("AllTitles") 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles " & _ 
 "ORDER BY ytd_sales DESC" 
 qdfPassThrough.ReturnsRecords = True 
 
 ' Create a temporary QueryDef object to retrieve 
 ' data from the pass-through query. 
 Set qdfLocal = dbsCurrent.CreateQueryDef("") 
 qdfLocal.SQL = "SELECT TOP 5 title FROM AllTitles" 
 
 Set rstTopFive = qdfLocal.OpenRecordset() 
 
 ' Display results of queries. 
 With rstTopFive 
 strMessage = _ 
 "Our top 5 best-selling books are:" & vbCr 
 
 Do While Not .EOF 
 strMessage = strMessage & " " & !Title & _ 
 vbCr 
 .MoveNext 
 Loop 
 
 If .RecordCount > 5 Then 
 strMessage = strMessage & _ 
 "(There was a tie, resulting in " & _ 
 vbCr & .RecordCount & _ 
 " books in the list.)" 
 End If 
 
 MsgBox strMessage 
 .Close 
 End With 
 
 ' Delete new pass-through query because this is a 
 ' demonstration. 
 dbsCurrent.QueryDefs.Delete "AllTitles" 
 dbsCurrent.Close 
 
```

<span data-ttu-id="5d9b8-116">この例では、 **ReturnsRecords** プロパティとカスタムの **LogMessages** プロパティを使用して、データおよびリモート サーバーで作成されたメッセージを返すパススルー クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="5d9b8-116">This example uses the **ReturnsRecords** property and the custom **LogMessages** property to create a pass-through query that will return data and any messages generated by the remote server.</span></span>

```vb 
Sub LogMessagesX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsCurrent As Database 
 Dim qdfTemp As QueryDef 
 Dim prpNew As Property 
 Dim rstTemp As Recordset 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 Set dbsCurrent = wrkAcc.OpenDatabase("DB1.mdb") 
 
 ' Create a QueryDef that will log any messages from the 
 ' server in temporary tables. 
 Set qdfTemp = dbsCurrent.CreateQueryDef("NewQueryDef") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfTemp.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfTemp.SQL = "SELECT * FROM stores" 
 qdfTemp.ReturnsRecords = True 
 Set prpNew = qdfTemp.CreateProperty("LogMessages", _ 
 dbBoolean, True) 
 qdfTemp.Properties.Append prpNew 
 
 ' Execute query and display results. 
 Set rstTemp = qdfTemp.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfTemp.Name 
 dbsCurrent.Close 
 wrkAcc.Close 
 
End Sub 
 
```

