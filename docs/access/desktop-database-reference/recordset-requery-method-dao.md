---
title: Recordset.Requery メソッド (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: bd6f2fdf7d1f8ba9fc47c6223a8f872a655a1e3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307624"
---
# <a name="recordsetrequery-method-dao"></a>Recordset.Requery メソッド (DAO)

**適用先:** Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行して、そのオブジェクトのデータを更新します。

## <a name="syntax"></a>構文

*式* .Requery(***NewQueryDef***)

*式* **Recordset** オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須 / オプション </p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NewQueryDef</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>
            <a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトの <strong>Name</strong> プロパティの値を表します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Recordset** が最新のデータを含んでいるかこの方法を使って確認します。 このメソッドでは、現在のクエリ パラメーターを使用するか、または (Microsoft Access ワークスペースの場合)、newquerydef 引数で指定された新しいクエリ を使用して、現在の**Recordset**にデータが再読み込みされます。

newquerydef 引数を指定しない場合、 **Recordset** に対するデータの再読み込みは、その **Recordset** に最初にデータが読み込まれたときと同じクエリ定義とパラメーターに基づいて行われます。 基になるデータに変更があった場合は、この再読み込み時に反映されます。 **QueryDef** を使用して **Recordset** を作成していない場合は、 **Recordset** が最初から再作成されます。

newquerydef 引数に元の **QueryDef**を指定した場合は、**QueryDef** で指定されたパラメーターを使用して **Recordset** が再取得されます。 この再読み込み中に、基になるデータの変更が反映されます。 クエリ パラメーターの値に対する変更を **Recordset** に反映するには、newquerydef 引数を指定する必要があります。

最初に **Recordset** を作成したときとは異なる **QueryDef** を指定した場合、**Recordset** は最初から再作成されます。


            **Requery** を使用すると、**Recordset** 内の最初のレコードがカレント レコードとなります。

**Requery** メソッドは、 [**Restartable**](recordset-restartable-property-dao.md) プロパティが **False** に設定されているダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトでは使用できません。 しかし、オプションの newquerydef 引数を指定した場合は、 **Restartable** プロパティが無視されます。

**Requery**メソッドを使用した後に、**Recordset**オブジェクトの**[BOF](recordset-bof-property-dao.md)** と**[EOF](recordset-eof-property-dao.md)** プロパティの両方の設定が**True** になった場合、クエリはレコードを返さず、**Recordset**にデータは含まれません。

## <a name="example"></a>例

この例では、**Requery** メソッドを使用して、基になるデータが変更された後にクエリを更新する方法を示します。

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

この例では、**Requery** メソッドを使用して、クエリ パラメーターが変更された後にクエリを更新する方法を示します。

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

