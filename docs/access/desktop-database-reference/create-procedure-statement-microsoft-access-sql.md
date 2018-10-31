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
ms.openlocfilehash: 573ec86a573697ebe52886535f8544bbaab61d7d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861465"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>CREATE PROCEDURE ステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013 

ストアド プロシージャを作成します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Jet データベース以外のデータベースでは CREATE PROCEDURE 句や DDL (データ定義言語) ステートメントを使用できません。

## <a name="syntax"></a>構文

プロシージャの作成*手順* \[ *param1 のデータ型*\[、*パラメーター 2 のデータ型*\[をしています.\] \]として連結

CREATE PROCEDURE ステートメントには次の指定項目があります。

|指定項目|説明|
|:---|:----------|
|*procedure*|プロシージャ名。名前付け規則に従った名前を指定します。|
|*param1*、*param2*|1 以上 255 個までのフィールド名またはパラメーター。たとえば、次のように指定します。
<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>パラメーターの詳細については、[パラメーター](parameters-declaration-microsoft-access-sql.md)を参照してください。|
|*datatype*|[Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。|
|*sqlstatement*|SELECT、UPDATE、DELETE、INSERT、CREATE TABLE、DROP TABLE などの SQL ステートメントを指定します。|


## <a name="remarks"></a>解説

SQL のプロシージャは、プロシージャ名を指定する PROCEDURE 句、パラメーター定義のリスト (省略可能)、および 1 つの SQL ステートメントで構成されます。

プロシージャ名は、既存のテーブル名と同じ名前を使用することはできません。

## <a name="example"></a>使用例

この例では、クエリ CategoryList、名前を指定し、SELECT ステートメントの例である EnumFields プロシージャを呼び出します。

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
