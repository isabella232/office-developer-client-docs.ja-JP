---
title: Recordset2.Requery メソッド (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: dc752105535f8a93a1b771eca8cfcf1dae11c1d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615068"
---
# <a name="recordset2requery-method-dao"></a>Recordset2.Requery メソッド (DAO)

**適用先:** Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行して、そのオブジェクトのデータを更新します。

## <a name="syntax"></a>構文

*式* .Requery(***NewQueryDef***)

*式* Recordset2 オブジェクトを **表す変数** 。

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
<th><p>必須かどうか</p></th>
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

このメソッドを使用して、**Recordset** に確実に最新のデータが含まれるようにします。このメソッドでは、現在のクエリ パラメーターを使用するか、または引数 newquerydef で指定された新しいクエリ (Microsoft Access ワークスペースの場合) を使用して、現在の **Recordset** に再度データを読み込みます。

newquerydef 引数を指定しない場合、 **Recordset** に対するデータの再読み込みは、その **Recordset** に最初にデータが読み込まれたときと同じクエリ定義とパラメーターに基づいて行われます。 基になるデータに変更があった場合は、この再読み込み時に反映されます。 **QueryDef** を使用して **Recordset** を作成していない場合は、 **Recordset** が最初から再作成されます。

newquerydef 引数に元の **QueryDef** を指定した場合は、**QueryDef** で指定されたパラメーターを使用して **Recordset** が再取得されます。 この再読み込み中に、基になるデータの変更が反映されます。 クエリ パラメーターの値に対する変更を **Recordset** に反映するには、newquerydef 引数を指定する必要があります。

最初に **Recordset** を作成したときとは異なる **QueryDef** を指定した場合、**Recordset** は最初から再作成されます。


            **Requery** を使用すると、**Recordset** 内の最初のレコードがカレント レコードとなります。

**Requery** メソッドは、 [**Restartable**](recordset2-restartable-property-dao.md) プロパティが **False** に設定されているダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトでは使用できません。 しかし、オプションの newquerydef 引数を指定した場合は、 **Restartable** プロパティが無視されます。

**Requery** メソッドを使用した後に、**Recordset** オブジェクトの **[BOF](recordset2-bof-property-dao.md)** と **[EOF](recordset2-eof-property-dao.md)** プロパティの両方の設定が **True** になった場合、クエリはレコードを返さず、**Recordset** にデータは含まれません。

## <a name="example"></a>例

この例では、**Requery** メソッドを使用して、基になるデータが変更された後にクエリを更新する方法を示します。

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
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
 Dim rstView As Recordset2 
 
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

