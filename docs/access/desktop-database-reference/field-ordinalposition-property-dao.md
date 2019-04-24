---
title: OrdinalPosition プロパティ (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d45f0362831d91b83b3a2449affbbfb5ac2b4e51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293036"
---
# <a name="fieldordinalposition-property-dao"></a><span data-ttu-id="f25b9-102">OrdinalPosition プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="f25b9-102">Field.OrdinalPosition property (DAO)</span></span>


<span data-ttu-id="f25b9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f25b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f25b9-104">**[Fields](fields-collection-dao.md)** コレクション内の**[Field](field-object-dao.md)** オブジェクトの相対位置を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="f25b9-104">Sets or returns the relative position of a **[Field](field-object-dao.md)** object within a **[Fields](fields-collection-dao.md)** collection.</span></span> <span data-ttu-id="f25b9-105">.</span><span class="sxs-lookup"><span data-stu-id="f25b9-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="f25b9-106">構文</span><span class="sxs-lookup"><span data-stu-id="f25b9-106">Syntax</span></span>

<span data-ttu-id="f25b9-107">*式*。OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="f25b9-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="f25b9-108">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f25b9-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f25b9-109">注釈</span><span class="sxs-lookup"><span data-stu-id="f25b9-109">Remarks</span></span>

<span data-ttu-id="f25b9-110">**Fields** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="f25b9-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="f25b9-111">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="f25b9-111">The default is 0.</span></span>

<span data-ttu-id="f25b9-112">**OrdinalPosition** プロパティを使用できるかどうかは、次の表に示すように、**Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="f25b9-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f25b9-113">Fields コレクションが属するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="f25b9-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="f25b9-114">OrdinalPosition プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="f25b9-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f25b9-115"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f25b9-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f25b9-116">サポートされない</span><span class="sxs-lookup"><span data-stu-id="f25b9-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f25b9-117"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f25b9-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f25b9-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f25b9-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f25b9-119"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f25b9-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f25b9-120">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="f25b9-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f25b9-121"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f25b9-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f25b9-122">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="f25b9-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f25b9-123"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f25b9-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f25b9-124">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="f25b9-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f25b9-125">通常、コレクションに追加するオブジェクトの順序位置は、そのオブジェクトを追加した順序になります。</span><span class="sxs-lookup"><span data-stu-id="f25b9-125">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object.</span></span> <span data-ttu-id="f25b9-126">最初に追加したオブジェクトが最初の位置 (0) に格納され、2 番目に追加したオブジェクトは 2 番目の位置 (1) に格納され、これ以降も同様です。</span><span class="sxs-lookup"><span data-stu-id="f25b9-126">The first appended object is in the first position (0), the second appended object is in the second position (1), and so on.</span></span> <span data-ttu-id="f25b9-127">最後に追加されたオブジェクトは、位置を表す count –1、count プロパティの設定値で指定された**[](containers-count-property-dao.md)** コレクション内のオブジェクトの数です。</span><span class="sxs-lookup"><span data-stu-id="f25b9-127">The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="f25b9-128">**OrdinalPosition** プロパティを使用すると、新しい **Field** オブジェクトの順序位置を指定可能で、これは、これらのオブジェクトをコレクションに追加するときの順序と異なります。</span><span class="sxs-lookup"><span data-stu-id="f25b9-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="f25b9-129">これにより、テーブル、クエリ、およびレコードセットをアプリケーションで使用するときのフィールドの順序を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f25b9-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="f25b9-130">たとえば、選択\*クエリでフィールドが返される順序は、現在の**OrdinalPosition**プロパティの値によって決まります。</span><span class="sxs-lookup"><span data-stu-id="f25b9-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="f25b9-131">**OrdinalPosition** プロパティを任意の正の整数に設定することにより、レコードセットにフィールドが返される順序を永続的にリセットできます。</span><span class="sxs-lookup"><span data-stu-id="f25b9-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="f25b9-p104">同じコレクション内の複数の **Field** オブジェクトが同じ **OrdinalPosition** プロパティ値を持つことが可能で、この場合、これらのオブジェクトの順序はアルファベット順になります。たとえば、Age という名前のフィールドを 4 に設定し、2 番目の Weight という名前のフィールドも 4 に設定すると、Age の後に Weight が返されます。</span><span class="sxs-lookup"><span data-stu-id="f25b9-p104">Two or more **Field** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="f25b9-p105">フィールド数から 1 を引いた数値より大きい数値を指定できます。フィールドは、最も大きい数値に対する相対的な順序で返されます。たとえば、フィールドの **OrdinalPosition** プロパティを 20 に設定し (フィールドは 5 つのみ)、他の 2 つのフィールドの **OrdinalPosition** プロパティをそれぞれ 10 と 30 に設定した場合、20 に設定されたフィールドは、10 に設定されたフィールドと 30 に設定されたフィールドの間に返されます。</span><span class="sxs-lookup"><span data-stu-id="f25b9-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>

> [!NOTE]
> <span data-ttu-id="f25b9-137">[tabledef](tabledef-object-dao.md)の**Fields**コレクションが更新されていない場合でも、tabledef から開いた[Recordset](recordset-object-dao.md)内の\*\*\*\* フィールドの順序には、 **tabledef**オブジェクトの**OrdinalPosition**データが反映されます。</span><span class="sxs-lookup"><span data-stu-id="f25b9-137">Even if the **Fields** collection of a [TableDef](tabledef-object-dao.md) has not been refreshed, the field order in a [Recordset](recordset-object-dao.md) opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object.</span></span> <span data-ttu-id="f25b9-138">テーブル タイプの **Recordset** には、基になるテーブルと同じ **OrdinalPosition** データが使用されますが、その他のタイプの **Recordset** には、**TableDef** オブジェクトの **OrdinalPosition** データによって指定される順序に従った、0 から始まる新しい **OrdinalPosition** データが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f25b9-138">A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span></span>

## <a name="example"></a><span data-ttu-id="f25b9-139">例</span><span class="sxs-lookup"><span data-stu-id="f25b9-139">Example</span></span>

<span data-ttu-id="f25b9-p107">次の例は、 **Recordset** オブジェクト内の **Field** オブジェクトの順序を制御するために、Employees **TableDef** オブジェクトの **OrdinalPosition** プロパティの値を変更します。すべての **Fields** オブジェクトの **OrdinalPosition** プロパティを 1 に設定することにより、 **Recordset** オブジェクトの **Fields** オブジェクトは順序がアルファベット順になります。 **Recordset** オブジェクトの **OrdinalPosition** 値は **TableDef** オブジェクトの値と一致しませんが、最終的な **TableDef** の変更には反映されます。</span><span class="sxs-lookup"><span data-stu-id="f25b9-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
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
