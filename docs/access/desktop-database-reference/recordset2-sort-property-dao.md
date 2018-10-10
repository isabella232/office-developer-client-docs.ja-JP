---
title: Recordset2.Sort プロパティ (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c7674f7513e75d0b03533dc165b49ac78d0461d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477442"
---
# <a name="recordset2sort-property-dao"></a>Recordset2.Sort プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013 

**[Recordset](recordset-object-dao.md)** オブジェクト内のレコードの並べ替え順序を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。並べ替え

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>備考

**Sort**プロパティを持つダイナセット: およびスナップショット タイプの**レコード セット**オブジェクトを使用できます。

オブジェクトに対してこのプロパティを設定すると、それ以降にそのオブジェクトから **Recordset** オブジェクトを作成するときに、レコードが並べ替えられます。 **Sort** プロパティの設定値は、 **[QueryDef](querydef-object-dao.md)** オブジェクトに指定されているいずれの並べ替え順序よりも優先されます。

既定の並べ替え順序は、昇順 (A ～ Z、0 ～ 100、あ～ん) です。

**Sort**プロパティをテーブル – または前方のみタイプの**Recordset**オブジェクトに適用されません。 テーブル タイプの**Recordset**オブジェクトを並べ替えるには、 **[Index](recordset2-index-property-dao.md)** プロパティを使用します。


> [!NOTE]
> <P>[!メモ] 多くの場合、並べ替え条件が含まれた SQL ステートメントを使用した方が、短時間で新しい <STRONG>Recordset</STRONG> オブジェクトを開くことができます。</P>



## <a name="example"></a>例

次の例では、 **Sort** プロパティの値を変更して新規の **Recordset** を作成することで、このプロパティの機能を示します。このプロシージャを実行するには、SortOutput 関数が必要です。

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
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
