---
title: Recordset.RecordCount プロパティ (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9bdc243aae48bd928468362cb86ca077f4abe52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307638"
---
# <a name="recordsetrecordcount-property-dao"></a>Recordset.RecordCount プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクト内のアクセス済みのレコード数、またはテーブル タイプの **Recordset** オブジェクト、あるいは **[TableDef](tabledef-object-dao.md)** オブジェクトの合計レコード数を取得します。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式* .RecordCount

*式* **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**RecordCount** プロパティを使用して、**Recordset** オブジェクトまたは **TableDef** オブジェクトのアクセス済みのレコード数を調べます。 ダイナセット タイプ、スナップショット タイプ、または前方スクロール タイプの **Recordset** オブジェクトでは、すべてのレコードがアクセス済みになるまで、そのオブジェクトに含まれている合計レコード数は **RecordCount** プロパティに示されません。 最後のレコードにアクセスした後、**Recordset** オブジェクト内または **TableDef** オブジェクト内にある削除されていないレコードの合計数が **RecordCount** プロパティに示されます。 最後のレコードがアクセスされるように強制するには、**Recordset** オブジェクトに対して **[MoveLast](recordset-movelast-method-dao.md)** メソッドを使用します。 また、SQL **Count** 関数を使用して、クエリから返される概算のレコード数を調べることもできます。

> [!NOTE]
> [!メモ] 新しく開いた **Recordset** オブジェクトに、 **MoveLast** メソッドを使用して値を設定するとパフォーマンスが低下します。 **Recordset** を開いた直後に正確な **RecordCount** プロパティの値が必要な場合を除き、コードの他の部分で **Recordset** オブジェクトに値が設定されるまで待機してから、 **RecordCount** プロパティを確認することをお勧めします。

ダイナセット タイプの **Recordset** オブジェクトにあるレコードをアプリケーションで削除すると、 **RecordCount** プロパティの値が減少します。ただし、他のユーザーが削除したレコードは、カレント レコードがその削除済みのレコードに移動するまで **RecordCount** プロパティに反映されません。 **RecordCount** プロパティの設定値に影響を与えるトランザクションを実行し、後でそのトランザクションをロールバックすると、残っているレコードの実際の数が **RecordCount** プロパティに反映されません。

基になるテーブルを変更しても、スナップショット タイプおよび前方スクロール タイプの **Recordset** オブジェクトの **RecordCount** プロパティに影響はありません。

レコードが格納されていない **Recordset** オブジェクトおよび **TableDef** オブジェクトは、 **RecordCount** プロパティが 0 に設定されます。

**Recordset** オブジェクトに対して **[Requery](recordset-requery-method-dao.md)** メソッドを使用すると、クエリがもう一度実行された場合と同じ状態に **RecordCount** プロパティが再設定されます。

## <a name="example"></a>例

この例では、さまざまな種類の **Recordsets** オブジェクトに値を設定する前と後の **RecordCount** プロパティの値を示します。

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
