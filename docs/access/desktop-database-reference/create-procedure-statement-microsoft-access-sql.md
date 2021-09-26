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
ms.localizationpriority: high
ms.openlocfilehash: b54d85a655bcb6ef60560583e8cbe1e2852c603e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569217"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>CREATE PROCEDURE ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013 

ストアド プロシージャを作成します。

> [!NOTE]
> Microsoft Access データベース エンジンは、Microsoft Jet データベース以外のデータベースでは CREATE PROCEDURE 句や DDL (データ定義言語) ステートメントを使用できません。

## <a name="syntax"></a>構文

CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement

CREATE PROCEDURE ステートメントでは、次の引数を使用します。

|パーツ|説明|
|:---|:----------|
|*procedure*|プロシージャの名前。名前付け規則に従った名前を指定します。|
|*param1*、*param2*|0 - 255 のフィールド名またはパラメーター。次に例を示します。<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>パラメーターの詳細については、「[PARAMETERS](parameters-declaration-microsoft-access-sql.md)」を参照してください。|
|*datatype*|
            [Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。|
|*sqlstatement*|SELECT、UPDATE、DELETE、INSERT、CREATE TABLE、DROP TABLE などの SQL ステートメント。|


## <a name="remarks"></a>注釈

SQL プロシージャは、プロシージャの名前を指定する PROCEDURE 句、オプションのパラメーター定義リスト、1 つの SQL ステートメントで構成されます。

プロシージャ名は、既存のテーブルの名前と同じにすることができません。

## <a name="example"></a>例

この例では、クエリを CategoryList と名付け、EnumFields プロシージャを呼び出します。EnumFields プロシージャについては、SELECT ステートメントの使用例を参照してください。

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
