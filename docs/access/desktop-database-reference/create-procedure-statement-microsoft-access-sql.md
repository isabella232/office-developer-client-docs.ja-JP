---
title: CREATE PROCEDURE ステートメント (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 2cd84f6e84d35cb24b2fd9b74146f3d401bbaba6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869443"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="807b8-102">CREATE PROCEDURE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="807b8-102">CREATE PROCEDURE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="807b8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="807b8-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="807b8-104">ストアド プロシージャを作成します。</span><span class="sxs-lookup"><span data-stu-id="807b8-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="807b8-105">[!メモ] Microsoft Access データベース エンジンは、Microsoft Jet データベース以外のデータベースでは CREATE PROCEDURE 句や DDL (データ定義言語) ステートメントを使用できません。</span><span class="sxs-lookup"><span data-stu-id="807b8-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="807b8-106">構文</span><span class="sxs-lookup"><span data-stu-id="807b8-106">Syntax</span></span>

<span data-ttu-id="807b8-107">プロシージャの作成*手順* \[ *param1 のデータ型*\[、*パラメーター 2 のデータ型*\[をしています.\] \]として連結</span><span class="sxs-lookup"><span data-stu-id="807b8-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span></span>

<span data-ttu-id="807b8-108">CREATE PROCEDURE ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="807b8-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="807b8-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="807b8-109">Part</span></span>|<span data-ttu-id="807b8-110">説明</span><span class="sxs-lookup"><span data-stu-id="807b8-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="807b8-111">*procedure*</span><span class="sxs-lookup"><span data-stu-id="807b8-111">*procedure*</span></span>|<span data-ttu-id="807b8-p101">プロシージャ名。名前付け規則に従った名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="807b8-p101">A name for the procedure. It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="807b8-114">*param1*、*param2*</span><span class="sxs-lookup"><span data-stu-id="807b8-114">*param1*, *param2*</span></span>|<span data-ttu-id="807b8-p102">1 以上 255 個までのフィールド名またはパラメーター。たとえば、次のように指定します。
</span><span class="sxs-lookup"><span data-stu-id="807b8-p102">From one to 255 field names or parameters. For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="807b8-117">パラメーターの詳細については、[パラメーター](parameters-declaration-microsoft-access-sql.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="807b8-117">For more information about parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="807b8-118">*datatype*</span><span class="sxs-lookup"><span data-stu-id="807b8-118">*datatype*</span></span>|<span data-ttu-id="807b8-119">[Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。</span><span class="sxs-lookup"><span data-stu-id="807b8-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="807b8-120">*sqlstatement*</span><span class="sxs-lookup"><span data-stu-id="807b8-120">*sqlstatement*</span></span>|<span data-ttu-id="807b8-121">SELECT、UPDATE、DELETE、INSERT、CREATE TABLE、DROP TABLE などの SQL ステートメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="807b8-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="807b8-122">解説</span><span class="sxs-lookup"><span data-stu-id="807b8-122">Remarks</span></span>

<span data-ttu-id="807b8-123">SQL のプロシージャは、プロシージャ名を指定する PROCEDURE 句、パラメーター定義のリスト (省略可能)、および 1 つの SQL ステートメントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="807b8-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="807b8-124">プロシージャ名は、既存のテーブル名と同じ名前を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="807b8-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="807b8-125">使用例</span><span class="sxs-lookup"><span data-stu-id="807b8-125">Example</span></span>

<span data-ttu-id="807b8-126">この例では、クエリ CategoryList、名前を指定し、SELECT ステートメントの例である EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="807b8-126">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
