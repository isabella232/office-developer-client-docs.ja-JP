---
title: Recordset.Requery メソッド (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb9eebad885b357c18d14c421826935cebbe4708
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478874"
---
# <a name="recordsetrequery-method-dao"></a>Recordset.Requery メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行することにより、オブジェクト内のデータを更新します。

## <a name="syntax"></a>構文

*式*です。(***NewQueryDef***) のクエリを再実行します。

*式***レコード セット**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NewQueryDef</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p><a href="querydef-object-dao.md"><strong>QueryDef</strong></a> オブジェクトの <strong>Name</strong> プロパティの値を表します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このメソッドは、 **Recordset** に確実に最新のデータが含まれるようにするために使用します。 このメソッドが現在のクエリ パラメーターを使用して、現在の**レコード セット**を再設定または引数 newquerydef で (Microsoft Access ワークスペース) で新しいファイルが提供されます。

Newquerydef 引数を省略する場合、最初の**レコード セット**を作成するために使用するパラメーターと同じクエリ定義に基づく**レコード セット**が再設定されます。 基になるデータに変更があった場合は、この再読み込み時に反映されます。 **QueryDef** を使用して **Recordset** を作成していない場合は、 **Recordset** が最初から再作成されます。

Newquerydef 引数に元の**クエリ定義**を指定する場合、**レコード セット**に対してクエリが実行**クエリ定義**で指定されたパラメーターを使用します。 基になるデータに変更があった場合は、この再読み込み時に反映されます。 **レコード セット**内のクエリ パラメーター値への変更を反映するためには、引数 newquerydef を指定してください。

最初に **Recordset** を作成したときとは異なる **QueryDef** を指定した場合、 **Recordset** は最初から再作成されます。

**Requery** を使用すると、 **Recordset** 内の最初のレコードがカレント レコードとなります。

**Requery** メソッドは、 [**Restartable**](recordset-restartable-property-dao.md) プロパティが **False** に設定されているダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトでは使用できません。 Newquerydef の省略可能な引数を指定する場合は、 **Restartable**プロパティは無視されます。

[Requery](recordset-bof-property-dao.md) を使用した後に、 **Recordset** オブジェクトの **[BOF](recordset-eof-property-dao.md)** プロパティと ****EOF**** プロパティの両方の設定が **True** になった場合、クエリによってレコードは返されておらず、 **Recordset** にはデータが含まれていません。

## <a name="example"></a>例

この例では、 **Requery** メソッドを使用して、基になるデータが変更された後にクエリを更新する方法を示します。

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

この例では、 **Requery** メソッドを使用して、クエリ パラメーターが変更された後にクエリを更新する方法を示します。

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

