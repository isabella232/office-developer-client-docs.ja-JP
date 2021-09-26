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
ms.localizationpriority: high
ms.openlocfilehash: c2bfa1366bda0e28520d941ea2b1d2bd8eaec310
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565171"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>PARAMETERS 宣言 (Microsoft Access SQL)


**適用先**: Access 2013、Office 2013

パラメーター クエリの中で使用する各パラメーターの名前とデータ型を宣言します。

## <a name="syntax"></a>構文

PARAMETERS *name datatype*\[、*name datatype*\[、...\]\]

PARAMETERS 宣言には、次の指定項目があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>指定項目</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>name</em></p></td>
<td><p>パラメーターの名前です。<strong>Parameter</strong> オブジェクトの <strong>Name</strong> プロパティに割り当てられ、<strong>Parameters</strong> コレクションでこのパラメーターを識別するために使用されます。アプリケーションでクエリを実行するときに、ダイアログ ボックスに表示される文字列として <em>name</em> を使用できます。角かっこ ([ ]) を使用して、スペースや句読点を含むテキストを囲みます。たとえば、[低価格] や [レポートの開始月は?] は、有効な <em>name</em> 引数です。</p></td>
</tr>
<tr class="even">
<td><p><em>datatype</em></p></td>
<td><p>
            <a href="sql-data-types.md">Microsoft Access SQL データ型</a>の 1 つ、またはその別名のうちの 1 つを指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

定期的に実行するクエリは、PARAMETERS 宣言を使用してパラメーター クエリにすると便利です。パラメーター クエリを使用すると、クエリの抽出条件の変更作業を自動化できます。パラメーター クエリでは、クエリを実行するたびにコードからパラメーターを指定する必要があります。

PARAMETERS 宣言は省略可能ですが、指定する場合は [SELECT](select-statement-microsoft-access-sql.md) ステートメントなどの他のステートメントよりも前に記述します。

この宣言で複数のパラメーターを指定する場合は、パラメーターとパラメーターの間をコンマで区切ります。次の例では、パラメーターを 2 つ指定しています。

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```


            [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句および [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) 句では、引数 *name* を使用できますが引数 *datatype* は使用できません。次の例では、ユーザーに 2 つのパラメーターの入力を求め、取得した抽出条件を Orders テーブルのレコードに適用します。

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>例

次の例では、ユーザーに役職の入力を求め、その役職をクエリの抽出条件として使用します。

[SELECT ステートメント](select-statement-microsoft-access-sql.md)の使用例で見つけることができる EnumFields プロシージャを呼び出します。

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
