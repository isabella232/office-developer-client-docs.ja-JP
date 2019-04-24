---
title: Recordset2. Requery メソッド (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307211"
---
# <a name="recordset2requery-method-dao"></a>Recordset2. Requery メソッド (DAO)

**適用先:** Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトの基になるクエリを再実行することにより、オブジェクト内のデータを更新します。

## <a name="syntax"></a>構文

*式*。Requery (***newquerydef***)

*式***Recordset2**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NewQueryDef</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><a href="querydef-object-dao.md"><strong>QueryDef</strong></a> オブジェクトの <strong>Name</strong> プロパティの値を表します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このメソッドは、 **Recordset** に確実に最新のデータが含まれるようにするために使用します。 このメソッドは、現在のクエリパラメーターまたは (Microsoft access ワークスペースでは) newquerydef 引数で指定された新しいレコードを使用して、現在の**Recordset**を再設定します。

newquerydef 引数を指定しない場合、 **recordset**には、最初に**recordset**にデータを格納するときに使用したのと同じクエリ定義とパラメーターに基づいてデータが再入力されます。 基になるデータに変更があった場合は、この再読み込み時に反映されます。 **QueryDef** を使用して **Recordset** を作成していない場合は、 **Recordset** が最初から再作成されます。

newquerydef 引数で元の**querydef**を指定すると、 **Recordset**は**QueryDef**で指定されたパラメーターを使用して再クエリされます。 基になるデータに変更があった場合は、この再読み込み時に反映されます。 **Recordset**内のクエリパラメーター値に加えられた変更を反映するには、newquerydef 引数を指定する必要があります。

最初に **Recordset** を作成したときとは異なる **QueryDef** を指定した場合、 **Recordset** は最初から再作成されます。

**Requery** を使用すると、 **Recordset** 内の最初のレコードがカレント レコードとなります。

**Requery** メソッドは、 [**Restartable**](recordset2-restartable-property-dao.md) プロパティが **False** に設定されているダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトでは使用できません。 ただし、省略可能な newquerydef 引数を指定すると、再**起動**可能なプロパティは無視されます。

**Requery**メソッドを使用した後に、 **recordset**オブジェクトの**[BOF](recordset2-bof-property-dao.md)** プロパティと**[EOF](recordset2-eof-property-dao.md)** プロパティの両方の設定が**True**になった場合、クエリはレコードを返さなかったため、 **recordset**にはデータが含まれていません。

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

この例では、 **Requery** メソッドを使用して、クエリ パラメーターが変更された後にクエリを更新する方法を示します。

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

