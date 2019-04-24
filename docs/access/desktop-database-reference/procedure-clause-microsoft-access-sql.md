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
# <a name="procedure-clause-microsoft-access-sql"></a>PROCEDURE 句 (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

クエリの名前と省略可能なパラメーターを定義します。

> [!NOTE]
> [!メモ] PROCEDURE 句は PROCEDURE ステートメントに換わりました。現在も PROCEDURE 句はサポートされていますが、PROCEDURE ステートメントは PROCEDURE 句の機能も備えているため、こちらを使用することを推奨します。

## <a name="syntax"></a>構文

プロシージャ*名* \[ *param1 データ*\[型、 *param2 datatype*\[、...\]\]

PROCEDURE 句には、次の指定項目があります。

|パーツ |説明 |
|:----|:-----------|
|*name* |プロシージャ名。 名前付け規則に従った名前を指定します。|
|*param1*、 *param2* |1 つ以上のフィールド名またはパラメーター。 たとえば、次のように指定します。<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>パラメーターの詳細については、「 [parameters](parameters-declaration-microsoft-access-sql.md)」を参照してください。|
|*datatype* | [Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。 |


## <a name="remarks"></a>注釈

SQL のプロシージャは、プロシージャ名を指定する PROCEDURE 句、パラメーター定義のリスト (省略可能)、および 1 つの SQL ステートメントで構成されます。 たとえば、プロシージャの Get\_part\_番号は、指定されたパーツ番号を取得するクエリを実行する場合があります。

> [!NOTE]
> - 句に複数のフィールド定義が含まれている場合 (つまり、*パラメータタイプ*のペア)、それらはコンマで区切ります。
> - PROCEDURE 句に続けて [SELECT](select-statement-microsoft-access-sql.md) や [UPDATE](update-statement-microsoft-access-sql.md) などの SQL ステートメントを記述する必要があります。

## <a name="example"></a>例

この例では、クエリカテゴリリストに名前を指定し、enumfields プロシージャを呼び出します。この例では、select ステートメントの使用例を参照してください。

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
