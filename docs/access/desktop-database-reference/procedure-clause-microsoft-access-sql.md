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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726317"
---
# <a name="procedure-clause-microsoft-access-sql"></a>PROCEDURE 句 (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

クエリの名前と省略可能なパラメーターを定義します。

> [!NOTE]
> [!メモ] PROCEDURE 句は PROCEDURE ステートメントに換わりました。現在も PROCEDURE 句はサポートされていますが、PROCEDURE ステートメントは PROCEDURE 句の機能も備えているため、こちらを使用することを推奨します。

## <a name="syntax"></a>構文

プロシージャ*名* \[ *param1 のデータ型*\[、*パラメーター 2 のデータ型*\[をしています.\]\]

PROCEDURE 句には、次の指定項目があります。

|指定項目 |説明 |
|:----|:-----------|
|*name* |プロシージャ名。名前付け規則に従った名前を指定します。|
|*param1*、*param2* |1 つ以上のフィールド名またはパラメーター。たとえば、次のように指定します。
<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>パラメーターの詳細については、[パラメーター](parameters-declaration-microsoft-access-sql.md)を参照してください。|
|*datatype* | [Microsoft Access SQL データ型](sql-data-types.md)の 1 つ、またはその別名のうちの 1 つを指定します。 |


## <a name="remarks"></a>解説

SQL のプロシージャは、プロシージャ名を指定する PROCEDURE 句、パラメーター定義のリスト (省略可能)、および 1 つの SQL ステートメントで構成されます。 Get プロシージャなど、\_パーツ\_番号は、特定の部品番号を取得するクエリを実行可能性があります。

> [!NOTE]
> - フィールド定義 (引数 param と datatype の対) を複数指定する場合は、それらをコンマで区切ってください。
> - PROCEDURE 句に続けて [SELECT](select-statement-microsoft-access-sql.md) や [UPDATE](update-statement-microsoft-access-sql.md) などの SQL ステートメントを記述する必要があります。

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
