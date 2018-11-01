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
ms.openlocfilehash: 451f2d1045b900460a24533ca49579bd9252f456
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881511"
---
# <a name="field2ordinalposition-property-dao"></a><span data-ttu-id="a7717-102">Field2.OrdinalPosition プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7717-102">Field2.OrdinalPosition Property (DAO)</span></span>


<span data-ttu-id="a7717-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a7717-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a7717-p101">[**Fields**](fields-collection-dao.md) コレクション内の **Field2** オブジェクトの相対位置を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a7717-p101">Sets or returns the relative position of a **Field2** object within a **[Fields](fields-collection-dao.md)** collection. .</span></span>

## <a name="syntax"></a><span data-ttu-id="a7717-106">構文</span><span class="sxs-lookup"><span data-stu-id="a7717-106">Syntax</span></span>

<span data-ttu-id="a7717-107">*式*です。OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="a7717-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="a7717-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a7717-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7717-109">注釈</span><span class="sxs-lookup"><span data-stu-id="a7717-109">Remarks</span></span>

<span data-ttu-id="a7717-110">**Fields** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="a7717-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="a7717-111">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="a7717-111">The default is 0.</span></span>

<span data-ttu-id="a7717-112">**OrdinalPosition** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="a7717-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7717-113">Fields コレクションが属するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="a7717-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="a7717-114">OrdinalPosition プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7717-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7717-115"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a7717-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7717-116">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="a7717-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7717-117"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a7717-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7717-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a7717-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7717-119"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a7717-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7717-120">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a7717-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7717-121"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a7717-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7717-122">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="a7717-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7717-123"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a7717-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a7717-124">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="a7717-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7717-125">通常、コレクションに追加するオブジェクトの順序位置は、そのオブジェクトを追加した順序になります。</span><span class="sxs-lookup"><span data-stu-id="a7717-125">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object.</span></span> <span data-ttu-id="a7717-126">最初に追加したオブジェクトが最初の位置 (0) に格納され、2 番目に追加したオブジェクトは 2 番目の位置 (1) に格納され、これ以降も同様です。</span><span class="sxs-lookup"><span data-stu-id="a7717-126">The first appended object is in the first position (0), the second appended object is in the second position (1), and so on.</span></span> <span data-ttu-id="a7717-127">最後に追加したオブジェクトは、count-1、count は**[Count](containers-count-property-dao.md)** プロパティの設定値によって指定されたコレクション内のオブジェクトの数です。</span><span class="sxs-lookup"><span data-stu-id="a7717-127">The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="a7717-128">**OrdinalPosition** プロパティを使用して、コレクションに追加する順序とは異なるインデックスを新しい **Field2** オブジェクトに指定できます。</span><span class="sxs-lookup"><span data-stu-id="a7717-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field2** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="a7717-129">これにより、テーブル、クエリ、およびレコードセットをアプリケーションで使用するときのフィールドの順序を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a7717-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="a7717-130">選択でフィールドを取得する順序などの\*クエリは、現在の**OrdinalPosition**プロパティの値によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="a7717-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="a7717-131">**OrdinalPosition** プロパティを任意の正の整数に設定することにより、レコードセットにフィールドが返される順序を永続的にリセットできます。</span><span class="sxs-lookup"><span data-stu-id="a7717-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="a7717-p104">同じコレクションの 2 つ以上の **Field2** オブジェクトに同じ **OrdinalPosition** プロパティ値が設定できますが、その場合、それらのオブジェクトはアルファベット順に並べられます。たとえば、Age という名前のフィールドを 4 に設定し、Weight という名前のフィールドも 4 に設定すると、Weight の方が Age の後に返されます。</span><span class="sxs-lookup"><span data-stu-id="a7717-p104">Two or more **Field2** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="a7717-p105">フィールド数から 1 を引いた数値より大きい数値を指定できます。フィールドは、最も大きい数値に対する相対的な順序で返されます。たとえば、フィールドの **OrdinalPosition** プロパティを 20 に設定し (フィールドは 5 つのみ)、他の 2 つのフィールドの **OrdinalPosition** プロパティをそれぞれ 10 と 30 に設定した場合、20 に設定されたフィールドは、10 に設定されたフィールドと 30 に設定されたフィールドの間に返されます。</span><span class="sxs-lookup"><span data-stu-id="a7717-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a7717-p106">[!メモ] <A href="tabledef-object-dao.md"><STRONG>TableDef</STRONG></A> の <STRONG>Fields</STRONG> コレクションが更新されていない場合でも、 <A href="recordset-object-dao.md">TableDef</A> から開いた <STRONG><STRONG>Recordset</STRONG></STRONG> は、 <STRONG>TableDef</STRONG> オブジェクトの <STRONG>OrdinalPosition</STRONG> データを反映します。テーブル タイプの <STRONG>Recordset</STRONG> には、基になるテーブルと同じ <STRONG>OrdinalPosition</STRONG> データが使用されますが、その他のタイプの <STRONG>Recordset</STRONG> には、 <STRONG>TableDef</STRONG> オブジェクトの <STRONG>OrdinalPosition</STRONG> データによって指定される順序に従った、0 から始まる新しい <STRONG>OrdinalPosition</STRONG> データが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a7717-p106">Even if the <STRONG>Fields</STRONG> collection of a <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> has not been refreshed, the field order in a <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> opened from the <STRONG>TableDef</STRONG> will reflect the <STRONG>OrdinalPosition</STRONG> data of the <STRONG>TableDef</STRONG> object. A table-type <STRONG>Recordset</STRONG> will have the same <STRONG>OrdinalPosition</STRONG> data as the underlying table, but any other type of <STRONG>Recordset</STRONG> will have new <STRONG>OrdinalPosition</STRONG> data (starting with 0) that follow the order determined by the <STRONG>OrdinalPosition</STRONG> data of the <STRONG>TableDef</STRONG>.</span></span></P>



## <a name="example"></a><span data-ttu-id="a7717-139">例</span><span class="sxs-lookup"><span data-stu-id="a7717-139">Example</span></span>

<span data-ttu-id="a7717-p107">次の使用例は、作成される **Recordset** の **Field2** の順序を制御するために、Employees テーブルの **TableDef** の **OrdinalPosition** プロパティの値を変更します。すべての **Fields** の **OrdinalPosition** プロパティを 1 に設定することにより、作成されるすべての **Recordset** の **Fields** オブジェクトはアルファベット順に並べ替えられます。 **Recordset** の **OrdinalPosition** プロパティの値は、 **TableDef** の値と一致するのではなく、 **TableDef** の変更の最終結果を反映しているだけです。</span><span class="sxs-lookup"><span data-stu-id="a7717-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field2** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

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
