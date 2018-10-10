---
title: Recordset.RecordCount プロパティ (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb3d73cc236821d56e2151d80cf0e0aba241b8c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477309"
---
# <a name="recordsetrecordcount-property-dao"></a>Recordset.RecordCount プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクト内のアクセス済みのレコード数、またはテーブル タイプの **Recordset** オブジェクト、あるいは **[TableDef](tabledef-object-dao.md)** オブジェクトの合計レコード数を取得します。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。RecordCount

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**RecordCount** プロパティを使用して、 **Recordset** オブジェクトまたは **TableDef** オブジェクトのアクセス済みのレコード数を調べます。 ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトでレコードの数が含まれているすべてのレコードがアクセス済みになるまで**RecordCount**プロパティに示されません。 最後のレコードにアクセスすると、 **Recordset** オブジェクトまたは **TableDef** オブジェクトにある、削除されていないレコードの合計数が **RecordCount** プロパティに示されます。 最後のレコードを強制的にアクセス済みにするには、 [Recordset](recordset-movelast-method-dao.md) オブジェクトに対して ****MoveLast**** メソッドを使用します。 また、SQL の **Count** 関数を使用して、クエリから返される概算のレコード数を調べることもできます。


> [!NOTE]
> <P>[!メモ] 新しく開いた <STRONG>Recordset</STRONG> オブジェクトに、 <STRONG>MoveLast</STRONG> メソッドを使用して値を設定するとパフォーマンスが低下します。 <STRONG>Recordset</STRONG> を開いた直後に正確な <STRONG>RecordCount</STRONG> プロパティの値が必要な場合を除き、コードの他の部分で <STRONG>Recordset</STRONG> オブジェクトに値が設定されるまで待機してから、 <STRONG>RecordCount</STRONG> プロパティを確認することをお勧めします。</P>



ダイナセット タイプの **Recordset** オブジェクトにあるレコードをアプリケーションで削除すると、 **RecordCount** プロパティの値が減少します。ただし、他のユーザーが削除したレコードは、カレント レコードがその削除済みのレコードに移動するまで **RecordCount** プロパティに反映されません。 **RecordCount** プロパティの設定値に影響を与えるトランザクションを実行し、後でそのトランザクションをロールバックすると、残っているレコードの実際の数が **RecordCount** プロパティに反映されません。

スナップショット: または前方のみタイプの**Recordset**オブジェクトの**RecordCount**プロパティは、基になるテーブルの変更の影響を受けません。

レコードが格納されていない **Recordset** オブジェクトおよび **TableDef** オブジェクトは、 **RecordCount** プロパティが 0 に設定されます。

[Recordset](recordset-requery-method-dao.md) オブジェクトに対して ****Requery**** メソッドを使用すると、クエリがもう一度実行された場合と同じ設定値に **RecordCount** プロパティが再設定されます。

## <a name="example"></a>例

以下の使用例は、さまざまな種類の **Recordsets** オブジェクトに値を設定する前と後の **RecordCount** プロパティの値を示します。

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
