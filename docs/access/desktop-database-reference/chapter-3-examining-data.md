---
title: '3 章: データを調べる'
TOCTitle: 'Chapter 3: Examining Data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 481fbc3bc39f184aeefe6738ac8d2a80fcd1d93f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477846"
---
# <a name="chapter-3-examining-data"></a>3 章: データを調べる


**適用されます**Access 2013 |。Office 2013

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
名 = [商品コード]</p></th>
<th><p>フィールド 1<br />
名 = [商品名]</p></th>
<th><p>フィールド 2<br />
名 = [単価]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>7</p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="even">
<td><p>14</p></td>
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


次のセクションでは、このサンプル **Recordset** でのカーソルの現在の位置の確認方法について説明します。

