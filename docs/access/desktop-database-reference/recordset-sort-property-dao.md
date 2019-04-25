---
title: Recordset.Sort プロパティ (DAO)
TOCTitle: Sort Property
ms:assetid: 9be9bf62-f713-537e-4df0-3a54d485a523
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198077(v=office.15)
ms:contentKeyID: 48546582
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053063
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 630efdc4da5a9064f9dd9055e3ceabc0283d6d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307582"
---
# <a name="recordsetsort-property-dao"></a>Recordset.Sort プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトのレコードの並べ替え順序を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .Sort

*式* **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Sort** プロパティは、ダイナセット タイプおよびスナップショット タイプの **Recordset** オブジェクトで使用できます。

オブジェクトにこのプロパティを設定すると、そのオブジェクトから後続の **Recordset** オブジェクトが作成されたときに並べ替えが行われます。**Sort** プロパティを設定すると、**[QueryDef](querydef-object-dao.md)** オブジェクトに指定された並べ替え順序が無効になります。

並べ替え順序を指定しない場合は、昇順 (A ～ Z、0 ～ 100、あ～ん) になります。

**Sort** プロパティは、テーブル タイプまたは前方スクロール タイプの **Recordset** オブジェクトには適用されません。 テーブル タイプの **Recordset** オブジェクトを並べ替えるには、**[Index](recordset-index-property-dao.md)** プロパティを使用します。

> [!NOTE]
> 多くの場合、並べ替え条件を含む SQL ステートメントを使用すると、新規の **Recordset** オブジェクトをより短時間で開くことができます。

## <a name="example"></a>例

次の例では、**Sort** プロパティの値を変更して新規の **Recordset** を作成することで、このプロパティの機能を示します。このプロシージャを実行するには、SortOutput 関数が必要です。

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstSortEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

選択するデータがわかっている場合は、SQL ステートメントを使用して **Recordset** を作成する方が一般に効率的です。次の例では、ただ 1 つの **Recordset** を作成して、前の例と同じ結果を得る方法を示します。

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
