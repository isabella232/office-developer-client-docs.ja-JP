---
title: Field2.OrdinalPosition プロパティ (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1672c893994c1257a3898304042816d859e83314
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927320"
---
# <a name="field2ordinalposition-property-dao"></a>Field2.OrdinalPosition プロパティ (DAO)


**適用されます**Access 2013、Office 2013。


[**Fields**](fields-collection-dao.md) コレクション内の **Field2** オブジェクトの相対位置を設定または取得します。

## <a name="syntax"></a>構文

*式*です。OrdinalPosition

*式***Field2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Fields** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。

既定値は 0 です。

**OrdinalPosition** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションが属するオブジェクト</p></th>
<th><p>OrdinalPosition プロパティ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>値の取得および設定が可能です。</p></td>
</tr>
</tbody>
</table>


通常、コレクションに追加するオブジェクトの順序位置は、そのオブジェクトを追加した順序になります。 最初に追加したオブジェクトが最初の位置 (0) に格納され、2 番目に追加したオブジェクトは 2 番目の位置 (1) に格納され、これ以降も同様です。 最後に追加したオブジェクトは、count-1、count は**[Count](containers-count-property-dao.md)** プロパティの設定値によって指定されたコレクション内のオブジェクトの数です。

**OrdinalPosition** プロパティを使用して、コレクションに追加する順序とは異なるインデックスを新しい **Field2** オブジェクトに指定できます。 これにより、テーブル、クエリ、およびレコードセットをアプリケーションで使用するときのフィールドの順序を指定できます。 選択でフィールドを取得する順序などの\*クエリは、現在の**OrdinalPosition**プロパティの値によって決定されます。

**OrdinalPosition** プロパティを任意の正の整数に設定することにより、レコードセットにフィールドが返される順序を永続的にリセットできます。

同じコレクションの 2 つ以上の **Field2** オブジェクトに同じ **OrdinalPosition** プロパティ値が設定できますが、その場合、それらのオブジェクトはアルファベット順に並べられます。たとえば、Age という名前のフィールドを 4 に設定し、Weight という名前のフィールドも 4 に設定すると、Weight の方が Age の後に返されます。

フィールド数から 1 を引いた数値より大きい数値を指定できます。フィールドは、最も大きい数値に対する相対的な順序で返されます。たとえば、フィールドの **OrdinalPosition** プロパティを 20 に設定し (フィールドは 5 つのみ)、他の 2 つのフィールドの **OrdinalPosition** プロパティをそれぞれ 10 と 30 に設定した場合、20 に設定されたフィールドは、10 に設定されたフィールドと 30 に設定されたフィールドの間に返されます。


> [!NOTE]
> <P>[!メモ] <A href="tabledef-object-dao.md"><STRONG>TableDef</STRONG></A> の <STRONG>Fields</STRONG> コレクションが更新されていない場合でも、 <A href="recordset-object-dao.md">TableDef</A> から開いた <STRONG><STRONG>Recordset</STRONG></STRONG> は、 <STRONG>TableDef</STRONG> オブジェクトの <STRONG>OrdinalPosition</STRONG> データを反映します。テーブル タイプの <STRONG>Recordset</STRONG> には、基になるテーブルと同じ <STRONG>OrdinalPosition</STRONG> データが使用されますが、その他のタイプの <STRONG>Recordset</STRONG> には、 <STRONG>TableDef</STRONG> オブジェクトの <STRONG>OrdinalPosition</STRONG> データによって指定される順序に従った、0 から始まる新しい <STRONG>OrdinalPosition</STRONG> データが使用されます。</P>



## <a name="example"></a>例

次の使用例は、作成される **Recordset** の **Field2** の順序を制御するために、Employees テーブルの **TableDef** の **OrdinalPosition** プロパティの値を変更します。すべての **Fields** の **OrdinalPosition** プロパティを 1 に設定することにより、作成されるすべての **Recordset** の **Fields** オブジェクトはアルファベット順に並べ替えられます。 **Recordset** の **OrdinalPosition** プロパティの値は、 **TableDef** の値と一致するのではなく、 **TableDef** の変更の最終結果を反映しているだけです。

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
