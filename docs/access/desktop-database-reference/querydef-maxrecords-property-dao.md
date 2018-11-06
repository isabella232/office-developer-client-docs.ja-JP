---
title: QueryDef.MaxRecords プロパティ (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0156983a455c72e4046424def188e41b94705087
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998228"
---
# <a name="querydefmaxrecords-property-dao"></a>QueryDef.MaxRecords プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

ODBC データ ソースに対して実行するクエリから返されるレコードの最大数を設定または取得します。

## <a name="syntax"></a>構文

*式*です。MaxRecords

*式***クエリ定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

既定値は 0 で、この値は、返されるレコード数に制限がないことを示します。

**MaxRecords** に指定した行数が **[Recordset](recordset-object-dao.md)** のアプリケーションに返されると、 **Recordset** にクエリ条件を満たすレコードがさらに存在する場合でも、クエリ プロセッサはそれらのレコードを返しません。このプロパティは、クライアントのリソースに制限があり、大量のレコードを管理できない環境で役に立ちます。

> [!NOTE]
> [!メモ] **MaxRecords** プロパティは、ODBC データ ソースに対してのみ使用できます。

## <a name="example"></a>例

この例では、 **MaxRecords** プロパティを使用して、ODBC データ ソースに対するクエリによって返されるレコード数の制限を設定します。

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

