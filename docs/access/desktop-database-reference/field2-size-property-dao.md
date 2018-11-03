---
title: Field2.Size プロパティ (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 241233c65606df54feceb99903656d4d873b320b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930456"
---
# <a name="field2size-property-dao"></a><span data-ttu-id="a998d-102">Field2.Size プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a998d-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="a998d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a998d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a998d-104">**Field2** オブジェクトの最大サイズをバイト数で示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a998d-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a998d-105">構文</span><span class="sxs-lookup"><span data-stu-id="a998d-105">Syntax</span></span>

<span data-ttu-id="a998d-106">*式*です。サイズ</span><span class="sxs-lookup"><span data-stu-id="a998d-106">*expression* .Size</span></span>

<span data-ttu-id="a998d-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a998d-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a998d-108">注釈</span><span class="sxs-lookup"><span data-stu-id="a998d-108">Remarks</span></span>

<span data-ttu-id="a998d-109">**[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="a998d-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="a998d-p101">文字データを含むフィールド (メモ型 (Memo) フィールドを除く) では、 **Size** プロパティは、そのフィールドが保持できる最大文字数を示します。数値フィールドでは、 **Size** プロパティは保存に必要なバイト数を示します。</span><span class="sxs-lookup"><span data-stu-id="a998d-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="a998d-112">**Size** プロパティを使用できるかどうかは、次の表に示すように、 **Field2** オブジェクトが追加される **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="a998d-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a998d-113">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="a998d-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="a998d-114">使用例</span><span class="sxs-lookup"><span data-stu-id="a998d-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a998d-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a998d-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a998d-116">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="a998d-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a998d-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a998d-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a998d-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="a998d-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a998d-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a998d-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="a998d-120">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="a998d-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a998d-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a998d-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="a998d-122">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="a998d-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a998d-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a998d-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a998d-124">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="a998d-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a998d-p102">テキスト型 (Text) 以外のデータ型の **Field2** オブジェクトを作成した場合、 **Type** プロパティの設定値により **Size** プロパティの設定値が自動的に決まるため、設定する必要はありません。ただし、テキスト型 (Text) の **Field2** オブジェクトでは、 **Size** プロパティを最大テキスト サイズ (Microsoft Access データベース エンジン データベースの場合 255) までの任意の整数に設定できます。サイズを設定していない場合、フィールドはデータベースで許可されるサイズになります。</span><span class="sxs-lookup"><span data-stu-id="a998d-p102">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="a998d-p103">ロング バイナリ型 (Long Binary) とメモ型 (Memo) の **Field2** オブジェクトでは、 **Size** は常に 0 に設定されます。特定のレコードのデータのサイズを識別するには、 **Field2** オブジェクトの **FieldSize** プロパティを使用します。ロング バイナリ型 (Long Binary) またはメモ型 (Memo) のフィールドの最大サイズを制限するのは、システム リソースまたはデータベースが許可する最大サイズのみです。</span><span class="sxs-lookup"><span data-stu-id="a998d-p103">For Long Binary and Memo **Field2** objects, **Size** is always set to 0. Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="a998d-131">例</span><span class="sxs-lookup"><span data-stu-id="a998d-131">Example</span></span>

<span data-ttu-id="a998d-132">次の使用例は、Employees テーブルの **Field2** オブジェクトの名前とサイズを列挙することで、 **Size** プロパティの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="a998d-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
