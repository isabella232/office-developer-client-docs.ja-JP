---
title: '第 3 章: データの検査'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 29e882685fe06d98984d15a4d5bd7e517f794a6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618519"
---
# <a name="chapter-3-examining-data"></a>第 3 章: データの検査

**適用先**: Access 2013、Office 2013

2 章では、データ ソースのデータを **Recordset** オブジェクトとして取得する方法について説明しました。この章では、 **Recordset** 間を移動してそのデータを表示する方法を含め、 **Recordset** の詳細について説明します。

**Recordsets** には、簡単にレコードセット間を移動しその内容を調べられるように設計されたメソッドとプロパティがあります。プロバイダーがサポートする機能によっては、一部の **Recordset** のメソッドまたはプロパティを使用できない場合があります。 **Recordset** オブジェクトの機能をさらに調べるために、次のコードを使用して、Microsoft SQL Server 2000 上の Northwind サンプル データベースから取得した **Recordset** について考えてみましょう。

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

次の SQL クエリは、5 つの行 (レコード) と 3 つの列 (フィールド) を持つ **Recordset** を取得します。次の表に各行の値を示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>フィールド 0<br />
Name = ProductID</p></th>
<th><p>フィールド 1<br />
Name = ProductName</p></th>
<th><p>フィールド 2<br />
Name = UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>7 </p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="even">
<td><p>14 </p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Manjimup Dried Apples</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10.0000</p></td>
</tr>
</tbody>
</table>


次のセクションでは、このサンプル Recordset でカーソルの現在の位置を見つける方法について **説明します**。

この章では、次のトピックについて説明します。

- [カレント レコードの検索 (ADO)](locating-the-current-record.md)
- [データを移動する (ADO)](navigating-through-the-data.md)
- [Recordset 構造について (ADO)](understanding-recordset-structure.md)
