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
localization_priority: Normal
ms.openlocfilehash: 72f31c71e710cca79695a7221f0e033d18d2f420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301380"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="93576-102">PROCEDURE 句 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="93576-102">PROCEDURE clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="93576-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="93576-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93576-104">クエリの名前と省略可能なパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="93576-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="93576-p101">[!メモ] PROCEDURE 句は PROCEDURE ステートメントに換わりました。現在も PROCEDURE 句はサポートされていますが、PROCEDURE ステートメントは PROCEDURE 句の機能も備えているため、こちらを使用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="93576-p101">The PROCEDURE clause has been superseded by the PROCEDURE statement. Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="93576-107">構文</span><span class="sxs-lookup"><span data-stu-id="93576-107">Syntax</span></span>

<span data-ttu-id="93576-108">プロシージャ*名* \[ *param1 データ*\[型、 *param2 datatype*\[、...\]\]</span><span class="sxs-lookup"><span data-stu-id="93576-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="93576-109">PROCEDURE 句には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="93576-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="93576-110">パーツ</span><span class="sxs-lookup"><span data-stu-id="93576-110">Part</span></span> |<span data-ttu-id="93576-111">説明</span><span class="sxs-lookup"><span data-stu-id="93576-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="93576-112">*name*</span><span class="sxs-lookup"><span data-stu-id="93576-112">*name*</span></span> |<span data-ttu-id="93576-113">プロシージャ名。</span><span class="sxs-lookup"><span data-stu-id="93576-113">A name for the procedure.</span></span> <span data-ttu-id="93576-114">名前付け規則に従った名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93576-114">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="93576-115">*param1*、 *param2*</span><span class="sxs-lookup"><span data-stu-id="93576-115">*param1*, *param2*</span></span> |<span data-ttu-id="93576-116">1 つ以上のフィールド名またはパラメーター。</span><span class="sxs-lookup"><span data-stu-id="93576-116">One or more field names or parameters.</span></span> <span data-ttu-id="93576-117">たとえば、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="93576-117">For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="93576-118">パラメーターの詳細については、「 [parameters](parameters-declaration-microsoft-access-sql.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93576-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="93576-119">*datatype*</span><span class="sxs-lookup"><span data-stu-id="93576-119">*datatype*</span></span> | <span data-ttu-id="93576-120">[Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。</span><span class="sxs-lookup"><span data-stu-id="93576-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="93576-121">注釈</span><span class="sxs-lookup"><span data-stu-id="93576-121">Remarks</span></span>

<span data-ttu-id="93576-122">SQL のプロシージャは、プロシージャ名を指定する PROCEDURE 句、パラメーター定義のリスト (省略可能)、および 1 つの SQL ステートメントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="93576-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="93576-123">たとえば、プロシージャの Get\_part\_番号は、指定されたパーツ番号を取得するクエリを実行する場合があります。</span><span class="sxs-lookup"><span data-stu-id="93576-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="93576-124">句に複数のフィールド定義が含まれている場合 (つまり、*パラメータタイプ*のペア)、それらはコンマで区切ります。</span><span class="sxs-lookup"><span data-stu-id="93576-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="93576-125">PROCEDURE 句に続けて [SELECT](select-statement-microsoft-access-sql.md) や [UPDATE](update-statement-microsoft-access-sql.md) などの SQL ステートメントを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93576-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="93576-126">例</span><span class="sxs-lookup"><span data-stu-id="93576-126">Example</span></span>

<span data-ttu-id="93576-127">この例では、クエリカテゴリリストに名前を指定し、enumfields プロシージャを呼び出します。この例では、select ステートメントの使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93576-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
