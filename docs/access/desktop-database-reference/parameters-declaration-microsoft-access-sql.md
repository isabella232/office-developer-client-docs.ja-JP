---
title: PARAMETERS 宣言 (Microsoft Access SQL)
TOCTitle: PARAMETERS Declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8ef554aab94bd5771e1df3313d04a4fbe2c383b8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478302"
---
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="fbf0d-102">PARAMETERS 宣言 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fbf0d-102">PARAMETERS Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="fbf0d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbf0d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fbf0d-104">パラメーター クエリの中で使用する各パラメーターの名前とデータ型を宣言します。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf0d-105">構文</span><span class="sxs-lookup"><span data-stu-id="fbf0d-105">Syntax</span></span>

<span data-ttu-id="fbf0d-106">パラメーター*名のデータ型* \[、*名前のデータ型* \[、.\]\]</span><span class="sxs-lookup"><span data-stu-id="fbf0d-106">PARAMETERS *name datatype* \[, *name datatype* \[, …\]\]</span></span>

<span data-ttu-id="fbf0d-107">PARAMETERS 宣言には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbf0d-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="fbf0d-108">Part</span></span></p></th>
<th><p><span data-ttu-id="fbf0d-109">説明</span><span class="sxs-lookup"><span data-stu-id="fbf0d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbf0d-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="fbf0d-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="fbf0d-111">パラメーターの名前です。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-111">The name of the parameter.</span></span> <span data-ttu-id="fbf0d-112"><strong>パラメーター</strong>オブジェクトの<strong>Name</strong>プロパティに割り当てられており、<strong>パラメーター</strong>コレクション内のこのパラメーターを識別するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-112">Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection.</span></span> <span data-ttu-id="fbf0d-113"><em>名</em>は、アプリケーションがクエリを実行中にダイアログ ボックスで表示される文字列として使用できます。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-113">You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query.</span></span> <span data-ttu-id="fbf0d-114">スペースや句読点を含む文字列を囲む角かっこ () を使用します。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-114">Use brackets ([ ]) to enclose text that contains spaces or punctuation.</span></span> <span data-ttu-id="fbf0d-115">たとえば、[バーゲン プライス] [どの month? を含むレポートを開始する] とは、有効な<em>名前</em>の引数です。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-115">For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbf0d-116"><em>datatype</em></span><span class="sxs-lookup"><span data-stu-id="fbf0d-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="fbf0d-117"><a href="sql-data-types.md">Microsoft Access SQL データ型</a>の 1 つ、またはその別名のうちの 1 つを指定します。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fbf0d-118">解説</span><span class="sxs-lookup"><span data-stu-id="fbf0d-118">Remarks</span></span>

<span data-ttu-id="fbf0d-p102">定期的に実行するクエリは、PARAMETERS 宣言を使用してパラメーター クエリにすると便利です。パラメーター クエリを使用すると、クエリの抽出条件の変更作業を自動化できます。パラメーター クエリでは、クエリを実行するたびにコードからパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-p102">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query. A parameter query can help automate the process of changing query criteria. With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="fbf0d-122">PARAMETERS 宣言は省略可能ですが、指定する場合は [SELECT](select-statement-microsoft-access-sql.md) ステートメントなどの他のステートメントよりも前に記述します。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="fbf0d-p103">この宣言で複数のパラメーターを指定する場合は、パラメーターとパラメーターの間をコンマで区切ります。次の例では、パラメーターを 2 つ指定しています。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-p103">If the declaration includes more than one parameter, separate them with commas. The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="fbf0d-125">[場所](https://msdn.microsoft.com/library/ff195245\(v=office.15\))または[HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\))句の中では、*データ型*ではないですが、*名前*を使用できます。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-125">You can use *name* but not *datatype* in a [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) or [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) clause.</span></span> <span data-ttu-id="fbf0d-126">次の例では、ユーザーに 2 つのパラメーターの入力を求め、取得した抽出条件を Orders テーブルのレコードに適用します。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-126">The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="fbf0d-127">使用例</span><span class="sxs-lookup"><span data-stu-id="fbf0d-127">Example</span></span>

<span data-ttu-id="fbf0d-128">次の例では、ユーザーに役職の入力を求め、その役職をクエリの抽出条件として使用します。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="fbf0d-129">この例では、EnumFields プロシージャを呼び出します。EnumFields プロシージャについては、[SELECT ステートメント](select-statement-microsoft-access-sql.md)の使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fbf0d-129">This example calls the EnumFields procedure, which you can find in the [SELECT statement](select-statement-microsoft-access-sql.md) example.</span></span>

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
