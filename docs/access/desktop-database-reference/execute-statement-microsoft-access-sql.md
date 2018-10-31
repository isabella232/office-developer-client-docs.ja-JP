---
title: EXECUTE ステートメント (Microsoft Access SQL)
TOCTitle: EXECUTE statement (Microsoft Access SQL)
ms:assetid: 9ec4d9ee-db2a-0319-3ccf-c035d67a1496
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198330(v=office.15)
ms:contentKeyID: 48546667
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277471
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b5350d411fa5f8f689ae3051a8531f2cb298af56
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860288"
---
# <a name="execute-statement-microsoft-access-sql"></a><span data-ttu-id="8109b-102">EXECUTE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8109b-102">EXECUTE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="8109b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8109b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8109b-104">プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="8109b-104">Used to invoke the execution of a procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8109b-105">構文</span><span class="sxs-lookup"><span data-stu-id="8109b-105">Syntax</span></span>

<span data-ttu-id="8109b-106">*プロシージャ*の実行\[ *param1*\[、*パラメーター 2*\[をしています.\]\]</span><span class="sxs-lookup"><span data-stu-id="8109b-106">EXECUTE *procedure* \[*param1*\[, *param2*\[, …\]\]</span></span>

<span data-ttu-id="8109b-107">EXECUTE ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="8109b-107">The EXECUTE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8109b-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="8109b-108">Part</span></span></p></th>
<th><p><span data-ttu-id="8109b-109">説明</span><span class="sxs-lookup"><span data-stu-id="8109b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8109b-110"><em>procedure</em></span><span class="sxs-lookup"><span data-stu-id="8109b-110"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="8109b-111">実行するプロシージャの名前。</span><span class="sxs-lookup"><span data-stu-id="8109b-111">The name of the procedure that is to be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8109b-112"><em>param1, param2, ...</em></span><span class="sxs-lookup"><span data-stu-id="8109b-112"><em>param1, param2, …</em></span></span></p></td>
<td><p><span data-ttu-id="8109b-113">パラメーターの値はプロシージャで定義されます。</span><span class="sxs-lookup"><span data-stu-id="8109b-113">Values for the parameters defined by the procedure.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="8109b-114">例</span><span class="sxs-lookup"><span data-stu-id="8109b-114">Example</span></span>

<span data-ttu-id="8109b-115">この例では、クエリ CategoryList、名前を指定し、SELECT ステートメントの例である EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8109b-115">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        Execute EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
