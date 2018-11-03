---
title: パラメーター宣言 (Microsoft Access SQL)
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
ms.openlocfilehash: e906e90fd6f7bf6e26898ed5381ef687c2ee8514
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937344"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>パラメーター宣言 (Microsoft Access SQL)


**適用されます**Access 2013、Office 2013。

パラメーター クエリの中で使用する各パラメーターの名前とデータ型を宣言します。

## <a name="syntax"></a>構文

パラメーター*名のデータ型* \[、*名前のデータ型* \[、.\]\]

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
<td><p>パラメーターの名前です。 <strong>パラメーター</strong>オブジェクトの<strong>Name</strong>プロパティに割り当てられており、<strong>パラメーター</strong>コレクション内のこのパラメーターを識別するために使用します。 <em>名</em>は、アプリケーションがクエリを実行中にダイアログ ボックスで表示される文字列として使用できます。 スペースや句読点を含む文字列を囲む角かっこ () を使用します。 たとえば、[バーゲン プライス] [どの month? を含むレポートを開始する] とは、有効な<em>名前</em>の引数です。</p></td>
</tr>
<tr class="even">
<td><p><em>datatype</em></p></td>
<td><p><a href="sql-data-types.md">Microsoft Access SQL データ型</a>の 1 つ、またはその別名のうちの 1 つを指定します。</p></td>
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

[場所](https://msdn.microsoft.com/library/ff195245\(v=office.15\))または[HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\))句の中では、*データ型*ではないですが、*名前*を使用できます。 次の例では、ユーザーに 2 つのパラメーターの入力を求め、取得した抽出条件を Orders テーブルのレコードに適用します。

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>使用例

次の例では、ユーザーに役職の入力を求め、その役職をクエリの抽出条件として使用します。

[SELECT ステートメント](select-statement-microsoft-access-sql.md)の例である EnumFields プロシージャを呼び出します。

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
