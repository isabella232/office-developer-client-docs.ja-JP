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
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295405"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="160ee-102">CREATE PROCEDURE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="160ee-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="160ee-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="160ee-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="160ee-104">ストアド プロシージャを作成します。</span><span class="sxs-lookup"><span data-stu-id="160ee-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="160ee-105">Microsoft Access データベース エンジンは、Microsoft Jet データベース以外のデータベースでは CREATE PROCEDURE 句や DDL (データ定義言語) ステートメントを使用できません。</span><span class="sxs-lookup"><span data-stu-id="160ee-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="160ee-106">構文</span><span class="sxs-lookup"><span data-stu-id="160ee-106">Syntax</span></span>

<span data-ttu-id="160ee-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span><span class="sxs-lookup"><span data-stu-id="160ee-107">CREATE PROCEDURE procedure
    [param1 datatype[, param2 datatype[, …]] AS sqlstatement</span></span>

<span data-ttu-id="160ee-108">CREATE PROCEDURE ステートメントでは、次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="160ee-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="160ee-109">パーツ</span><span class="sxs-lookup"><span data-stu-id="160ee-109">Part</span></span>|<span data-ttu-id="160ee-110">説明</span><span class="sxs-lookup"><span data-stu-id="160ee-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="160ee-111">*procedure*</span><span class="sxs-lookup"><span data-stu-id="160ee-111">*procedure*</span></span>|<span data-ttu-id="160ee-112">プロシージャの名前。</span><span class="sxs-lookup"><span data-stu-id="160ee-112">A name for the procedure.</span></span> <span data-ttu-id="160ee-113">名前付け規則に従った名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="160ee-113">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="160ee-114">*param1*、*param2*</span><span class="sxs-lookup"><span data-stu-id="160ee-114">*param1*, *param2*</span></span>|<span data-ttu-id="160ee-115">0 ～ 255 のフィールド名またはパラメーター。</span><span class="sxs-lookup"><span data-stu-id="160ee-115">From one to 255 field names or parameters.</span></span> <span data-ttu-id="160ee-116">例:</span><span class="sxs-lookup"><span data-stu-id="160ee-116">For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="160ee-117">パラメーターの詳細については、「[PARAMETERS](parameters-declaration-microsoft-access-sql.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="160ee-117">For more information on parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="160ee-118">*datatype*</span><span class="sxs-lookup"><span data-stu-id="160ee-118">*datatype*</span></span>|<span data-ttu-id="160ee-119">
            [Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。</span><span class="sxs-lookup"><span data-stu-id="160ee-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="160ee-120">*sqlstatement*</span><span class="sxs-lookup"><span data-stu-id="160ee-120">*SQLStatement*</span></span>|<span data-ttu-id="160ee-121">SELECT、UPDATE、DELETE、INSERT、CREATE TABLE、DROP TABLE などの SQL ステートメント。</span><span class="sxs-lookup"><span data-stu-id="160ee-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="160ee-122">注釈</span><span class="sxs-lookup"><span data-stu-id="160ee-122">Remarks</span></span>

<span data-ttu-id="160ee-123">SQL プロシージャは、プロシージャの名前を指定する PROCEDURE 句、オプションのパラメーター定義リスト、1 つの SQL ステートメントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="160ee-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="160ee-124">プロシージャ名は、既存のテーブルの名前と同じにすることができません。</span><span class="sxs-lookup"><span data-stu-id="160ee-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="160ee-125">例</span><span class="sxs-lookup"><span data-stu-id="160ee-125">Example</span></span>

<span data-ttu-id="160ee-126">この例では、クエリを CategoryList と名付け、EnumFields プロシージャを呼び出します。EnumFields プロシージャについては、SELECT ステートメントの使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="160ee-126">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
