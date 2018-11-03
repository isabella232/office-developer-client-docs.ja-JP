---
title: PROCEDURE 句 (Microsoft Access SQL)
TOCTitle: PROCEDURE clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dd99fb241572f2e16eae914ba7d1dea31e1d097f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924261"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="2e94c-102">PROCEDURE 句 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="2e94c-102">PROCEDURE clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="2e94c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2e94c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e94c-104">クエリの名前と省略可能なパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="2e94c-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="2e94c-p101">[!メモ] PROCEDURE 句は PROCEDURE ステートメントに換わりました。現在も PROCEDURE 句はサポートされていますが、PROCEDURE ステートメントは PROCEDURE 句の機能も備えているため、こちらを使用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="2e94c-p101">The PROCEDURE clause has been superseded by the PROCEDURE statement. Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e94c-107">構文</span><span class="sxs-lookup"><span data-stu-id="2e94c-107">Syntax</span></span>

<span data-ttu-id="2e94c-108">プロシージャ*名* \[ *param1 のデータ型*\[、*パラメーター 2 のデータ型*\[をしています.\]\]</span><span class="sxs-lookup"><span data-stu-id="2e94c-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="2e94c-109">PROCEDURE 句には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="2e94c-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="2e94c-110">指定項目</span><span class="sxs-lookup"><span data-stu-id="2e94c-110">Part</span></span> |<span data-ttu-id="2e94c-111">説明</span><span class="sxs-lookup"><span data-stu-id="2e94c-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="2e94c-112">*name*</span><span class="sxs-lookup"><span data-stu-id="2e94c-112">*name*</span></span> |<span data-ttu-id="2e94c-p102">プロシージャ名。名前付け規則に従った名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e94c-p102">A name for the procedure. It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="2e94c-115">*param1*、*param2*</span><span class="sxs-lookup"><span data-stu-id="2e94c-115">*param1*, *param2*</span></span> |<span data-ttu-id="2e94c-p103">1 つ以上のフィールド名またはパラメーター。たとえば、次のように指定します。
</span><span class="sxs-lookup"><span data-stu-id="2e94c-p103">One or more field names or parameters. For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="2e94c-118">パラメーターの詳細については、[パラメーター](parameters-declaration-microsoft-access-sql.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e94c-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="2e94c-119">*datatype*</span><span class="sxs-lookup"><span data-stu-id="2e94c-119">*datatype*</span></span> | <span data-ttu-id="2e94c-120">[Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e94c-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="2e94c-121">解説</span><span class="sxs-lookup"><span data-stu-id="2e94c-121">Remarks</span></span>

<span data-ttu-id="2e94c-122">SQL のプロシージャは、プロシージャ名を指定する PROCEDURE 句、パラメーター定義のリスト (省略可能)、および 1 つの SQL ステートメントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="2e94c-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="2e94c-123">Get プロシージャなど、\_パーツ\_番号は、特定の部品番号を取得するクエリを実行可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2e94c-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="2e94c-124">フィールド定義 (引数 param と datatype の対) を複数指定する場合は、それらをコンマで区切ってください。</span><span class="sxs-lookup"><span data-stu-id="2e94c-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="2e94c-125">PROCEDURE 句に続けて [SELECT](select-statement-microsoft-access-sql.md) や [UPDATE](update-statement-microsoft-access-sql.md) などの SQL ステートメントを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e94c-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="2e94c-126">使用例</span><span class="sxs-lookup"><span data-stu-id="2e94c-126">Example</span></span>

<span data-ttu-id="2e94c-127">この例では、クエリ CategoryList、名前を指定し、SELECT ステートメントの例である EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e94c-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
