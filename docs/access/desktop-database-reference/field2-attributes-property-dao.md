---
title: Field2.Attributes プロパティ (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2456fb3741cfe5871b46e7937619b060fd350b09
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922400"
---
# <a name="field2attributes-property-dao"></a><span data-ttu-id="c1136-102">Field2.Attributes プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c1136-102">Field2.Attributes property (DAO)</span></span>


<span data-ttu-id="c1136-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c1136-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c1136-p101">**Field2** オブジェクトの 1 つまたは複数の特性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1136-p101">Sets or returns a value that indicates one or more characteristics of a **Field2** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1136-106">構文</span><span class="sxs-lookup"><span data-stu-id="c1136-106">Syntax</span></span>

<span data-ttu-id="c1136-107">*式*です。属性</span><span class="sxs-lookup"><span data-stu-id="c1136-107">*expression* .Attributes</span></span>

<span data-ttu-id="c1136-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c1136-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1136-109">注釈</span><span class="sxs-lookup"><span data-stu-id="c1136-109">Remarks</span></span>

<span data-ttu-id="c1136-110">この値は、 **Field2** オブジェクトで表されるフィールドの特性を指定するもので、以下の定数の組み合わせを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c1136-110">The value specifies characteristics of the field represented by the **Field2** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1136-111">定数</span><span class="sxs-lookup"><span data-stu-id="c1136-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="c1136-112">説明</span><span class="sxs-lookup"><span data-stu-id="c1136-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1136-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="c1136-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="c1136-114">新しいレコードのフィールド値は、一意の長整数型の値に自動的に増分され、変更はできません (Microsoft Access ワークスペースでは、Microsoft Office Access データベース エンジン データベース テーブルでのみサポート)。</span><span class="sxs-lookup"><span data-stu-id="c1136-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1136-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="c1136-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="c1136-p102">フィールドを降順 (Z ～ A、100 ～ 0、ん～あ) で並べ替えるオプションで、これは、<strong>Index</strong> オブジェクトの <strong>Fields</strong> コレクションの <strong>Field2</strong> オブジェクトのみに適用されます。この定数を省略すると、フィールドは昇順 (A ～ Z、0 ～ 100、あ～ん) で並べ替えられます。これは、<strong>Index</strong> フィールドおよび <strong>TableDef</strong> フィールドの既定値です (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c1136-p102">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field2</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object. If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order. This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1136-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="c1136-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="c1136-120">フィールド サイズは固定です (数値フィールドの既定)。</span><span class="sxs-lookup"><span data-stu-id="c1136-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1136-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="c1136-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="c1136-122">フィールドにはハイパーリンク情報が含まれます (メモ型フィールドのみ)。</span><span class="sxs-lookup"><span data-stu-id="c1136-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1136-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="c1136-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="c1136-124">レプリカのレプリケーション情報が保存される、削除できないタイプのフィールドです (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c1136-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1136-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="c1136-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="c1136-126">フィールド値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c1136-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1136-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="c1136-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="c1136-128">フィールド サイズは可変です (テキスト フィールドのみ)。</span><span class="sxs-lookup"><span data-stu-id="c1136-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1136-p103">コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。追加された **Field2** オブジェクトの場合、 **Attributes** プロパティを使用できるかどうかは、 **Fields** コレクションを含むオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c1136-p103">For an object not yet appended to a collection, this property is read/write. For an appended **Field2** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1136-131">Field オブジェクトの所属先</span><span class="sxs-lookup"><span data-stu-id="c1136-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="c1136-132">Attributes プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="c1136-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1136-133"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c1136-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c1136-134"><strong>Index</strong> オブジェクトが追加される <strong>TableDef</strong> オブジェクトが <strong>Database</strong> オブジェクトに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="c1136-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1136-135"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c1136-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c1136-136">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c1136-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1136-137"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c1136-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c1136-138">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c1136-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1136-139"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c1136-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c1136-140">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="c1136-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1136-141"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c1136-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c1136-142">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="c1136-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1136-p104">複数の属性を設定する場合は、該当する定数をまとめて組み合わせることができます。無効な値は、エラーを発生させずに無視されます。</span><span class="sxs-lookup"><span data-stu-id="c1136-p104">When you set multiple attributes, you can combine them by summing the appropriate constants. Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="c1136-145">例</span><span class="sxs-lookup"><span data-stu-id="c1136-145">Example</span></span>

<span data-ttu-id="c1136-146">次の使用例は、ノースウィンド データベースの **Field2**、 **Relation**、および **TableDef** の各オブジェクトの **Attributes** プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="c1136-146">This example displays the **Attributes** property for **Field2**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

