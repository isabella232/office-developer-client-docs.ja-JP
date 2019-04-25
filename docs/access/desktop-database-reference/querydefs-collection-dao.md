---
title: QueryDefs コレクション (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 3543d882e0584c35c88a5475032d9fe5505f516c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303235"
---
# <a name="querydefs-collection-dao"></a><span data-ttu-id="9bb9c-102">QueryDefs コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="9bb9c-102">QueryDefs Collection (DAO)</span></span>

<span data-ttu-id="9bb9c-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bb9c-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="9bb9c-104">**QueryDefs** コレクションには、Microsoft Access データベース エンジン データベースの **Database** オブジェクトのすべての **QueryDef** オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-104">A **QueryDefs** collection contains all **QueryDef** objects of a **Database** object in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bb9c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="9bb9c-105">Remarks</span></span>

<span data-ttu-id="9bb9c-106">新しい **QueryDef** オブジェクトを作成するには、 **CreateQueryDef** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-106">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="9bb9c-107">Microsoft Access ワークスペースで、引数  name に文字列を指定するか、新しい **QueryDef** オブジェクトの **Name** プロパティを明示的に長さ 0 の文字列以外に設定すると、 **QueryDefs** コレクションに自動的に追加されてディスクに保存される、永続的な **QueryDef** オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-107">In a Microsoft Access workspace, if you supply a string for the  name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non-zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="9bb9c-108">引数  name として長さ 0 の文字列を指定するか、 **Name** プロパティを長さ 0 の文字列に明示的に設定すると、一時的な **QueryDef** オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-108">Supplying a zero-length string as the  name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="9bb9c-109">コレクション内の **QueryDef** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-109">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="9bb9c-110">**QueryDefs** (0)</span><span class="sxs-lookup"><span data-stu-id="9bb9c-110">**QueryDefs**(0)</span></span>

<span data-ttu-id="9bb9c-111">**QueryDefs** (「名前」)</span><span class="sxs-lookup"><span data-stu-id="9bb9c-111">**QueryDefs**("name")</span></span>

<span data-ttu-id="9bb9c-112">**QueryDefs**\!\[名前\]</span><span class="sxs-lookup"><span data-stu-id="9bb9c-112">**QueryDefs**\!\[name\]</span></span>

<span data-ttu-id="9bb9c-113">一時的な **QueryDef** オブジェクトは、オブジェクトに割り当てたオブジェクト変数でのみ参照できます。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-113">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

## <a name="example"></a><span data-ttu-id="9bb9c-114">例</span><span class="sxs-lookup"><span data-stu-id="9bb9c-114">Example</span></span>

<span data-ttu-id="9bb9c-p102">この例では、新しい **QueryDef** オブジェクトを作成し、Northwind **Database** オブジェクトの **QueryDefs** コレクションに追加します。次に、**QueryDefs** コレクションおよび新しい **QueryDef** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-p102">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="9bb9c-117">この例では、**CreateQueryDef** メソッドを使用して、一時的と永続的な **QueryDef** の両方を作成して実行します。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-117">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="9bb9c-118">この手順を実行するには、GetrstTemp 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-118">The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

次の例は、パラメータ クエリを実行する方法を示しています。 <span data-ttu-id="9bb9c-120">Parameters コレクションは、クエリが実行される前に myActionQuery クエリの Organization パラメータを設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-120">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="9bb9c-121">**サンプル コードの提供元:** [Microsoft Access 2010 プログラマー用リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-121">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="9bb9c-122">次の例は、パラメーター クエリに基づく Recordset を開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-122">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

