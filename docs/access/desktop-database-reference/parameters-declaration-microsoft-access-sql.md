---
title: PARAMETERS 宣言 (Microsoft Access SQL)
TOCTitle: PARAMETERS declaration (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: d78a6c043e99af1ca50ca798b94088400fd09f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287868"
---
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="31976-102">PARAMETERS 宣言 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="31976-102">PARAMETERS Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="31976-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="31976-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31976-104">パラメーター クエリの中で使用する各パラメーターの名前とデータ型を宣言します。</span><span class="sxs-lookup"><span data-stu-id="31976-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="31976-105">構文</span><span class="sxs-lookup"><span data-stu-id="31976-105">Syntax</span></span>

<span data-ttu-id="31976-106">PARAMETERS *name datatype*\[、*name datatype*\[、...\]\]</span><span class="sxs-lookup"><span data-stu-id="31976-106">PARAMETERS *name datatype* \[ [, *name datatype* \[ [, …]]</span></span>

<span data-ttu-id="31976-107">PARAMETERS 宣言には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="31976-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31976-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="31976-108">Part</span></span></p></th>
<th><p><span data-ttu-id="31976-109">説明</span><span class="sxs-lookup"><span data-stu-id="31976-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31976-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="31976-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="31976-111">パラメーターの名前です。</span><span class="sxs-lookup"><span data-stu-id="31976-111">The name of the parameter.</span></span> <span data-ttu-id="31976-112"><strong>Parameter</strong> オブジェクトの <strong>Name</strong> プロパティに割り当てられ、<strong>Parameters</strong> コレクションでこのパラメーターを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31976-112">Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection.</span></span> <span data-ttu-id="31976-113">アプリケーションでクエリを実行するときに、ダイアログ ボックスに表示される文字列として <em>name</em> を使用できます。</span><span class="sxs-lookup"><span data-stu-id="31976-113">You can use  <em>name</em>  as a string that is displayed in a dialog box while your application runs the query.</span></span> <span data-ttu-id="31976-114">角かっこ ([ ]) を使用して、スペースや句読点を含むテキストを囲みます。</span><span class="sxs-lookup"><span data-stu-id="31976-114">Use brackets ([ ]) to enclose text that contains spaces or punctuation.</span></span> <span data-ttu-id="31976-115">たとえば、[低価格] や [レポートの開始月は?] は、有効な <em>name</em> 引数です。</span><span class="sxs-lookup"><span data-stu-id="31976-115">For example, [Low price] and [Begin report with which month?] are valid  <em>name</em>  arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31976-116"><em>datatype</em></span><span class="sxs-lookup"><span data-stu-id="31976-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="31976-117">
            <a href="sql-data-types.md">Microsoft Access SQL データ型</a>の 1 つ、またはその別名のうちの 1 つを指定します。</span><span class="sxs-lookup"><span data-stu-id="31976-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="31976-118">解説</span><span class="sxs-lookup"><span data-stu-id="31976-118">Remarks</span></span>

<span data-ttu-id="31976-p102">定期的に実行するクエリは、PARAMETERS 宣言を使用してパラメーター クエリにすると便利です。パラメーター クエリを使用すると、クエリの抽出条件の変更作業を自動化できます。パラメーター クエリでは、クエリを実行するたびにコードからパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31976-p102">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query. A parameter query can help automate the process of changing query criteria. With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="31976-122">PARAMETERS 宣言は省略可能ですが、指定する場合は [SELECT](select-statement-microsoft-access-sql.md) ステートメントなどの他のステートメントよりも前に記述します。</span><span class="sxs-lookup"><span data-stu-id="31976-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="31976-p103">この宣言で複数のパラメーターを指定する場合は、パラメーターとパラメーターの間をコンマで区切ります。次の例では、パラメーターを 2 つ指定しています。</span><span class="sxs-lookup"><span data-stu-id="31976-p103">If the declaration includes more than one parameter, separate them with commas. The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="31976-p104">
            [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句および [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) 句では、引数 \*name\* を使用できますが引数 \*datatype\* は使用できません。次の例では、ユーザーに 2 つのパラメーターの入力を求め、取得した抽出条件を Orders テーブルのレコードに適用します。</span><span class="sxs-lookup"><span data-stu-id="31976-p104">You can use *name* but not *datatype* in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) clause. The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="31976-127">例</span><span class="sxs-lookup"><span data-stu-id="31976-127">Example</span></span>

<span data-ttu-id="31976-128">次の例では、ユーザーに役職の入力を求め、その役職をクエリの抽出条件として使用します。</span><span class="sxs-lookup"><span data-stu-id="31976-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="31976-129">[SELECT ステートメント](select-statement-microsoft-access-sql.md)の使用例で見つけることができる EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="31976-129">This example calls the EnumFields procedure, which you can find in the [SELECT statement](select-statement-microsoft-access-sql.md) example.</span></span>

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
