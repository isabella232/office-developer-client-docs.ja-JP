---
title: Field.Size プロパティ (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e1e7d124e06331a043a28c71bcdc9707c4664738
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931331"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="c7e09-102">Field.Size プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c7e09-102">Field.Size property (DAO)</span></span>


<span data-ttu-id="c7e09-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c7e09-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c7e09-104">**[Field](field-object-dao.md)** オブジェクトの最大サイズをバイト数で示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c7e09-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e09-105">構文</span><span class="sxs-lookup"><span data-stu-id="c7e09-105">Syntax</span></span>

<span data-ttu-id="c7e09-106">*式*です。サイズ</span><span class="sxs-lookup"><span data-stu-id="c7e09-106">*expression* .Size</span></span>

<span data-ttu-id="c7e09-107">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c7e09-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e09-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c7e09-108">Remarks</span></span>

<span data-ttu-id="c7e09-109">**[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="c7e09-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="c7e09-p101">文字データを含むフィールド (メモ型フィールドを除く) の場合、 **Size** プロパティは、フィールドが保持できる最大文字数を示します。数値フィールドの場合、 **Size** プロパティは、格納に必要なバイト数を示します。</span><span class="sxs-lookup"><span data-stu-id="c7e09-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="c7e09-112">**Size** プロパティを使用するかどうかは、次の表に示すように、 **Field** オブジェクトの追加先の **Fields** コレクションを含むオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c7e09-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7e09-113">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="c7e09-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="c7e09-114">使用例</span><span class="sxs-lookup"><span data-stu-id="c7e09-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7e09-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="c7e09-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e09-116">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="c7e09-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7e09-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="c7e09-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e09-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c7e09-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7e09-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="c7e09-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e09-120">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c7e09-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7e09-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="c7e09-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e09-122">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="c7e09-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7e09-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="c7e09-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e09-124">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c7e09-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7e09-p102">テキスト型 (Text) 以外のデータ型で **Field** オブジェクトを作成する場合、 **[Type](field-type-property-dao.md)** プロパティの設定によって **Size** プロパティの設定が自動的に決まり、ユーザーが設定する必要はありません。ただし、テキスト型 (Text) のデータ型を持つ **Field** オブジェクトの場合、 **Size** を最大テキスト サイズ以内の任意の整数 (Microsoft Access データベースでは 255) に設定できます。サイズを指定しない場合、フィールドはデータベースで許容される最大サイズになります。</span><span class="sxs-lookup"><span data-stu-id="c7e09-p102">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="c7e09-p103">ロング バイナリ型 (Long Binary) とメモ型 (Memo) の **Field** オブジェクトの場合、 **Size** は常に 0 に設定されます。特定レコードのデータのサイズを確認するには、 [Field](field-fieldsize-property-dao.md) オブジェクトの \*\*\*\*FieldSize\*\*\*\* プロパティを使用します。ロング バイナリ型とメモ型のフィールドの最大サイズは、システム リソースまたはデータベースで許容される最大サイズによってのみ制限されます。</span><span class="sxs-lookup"><span data-stu-id="c7e09-p103">For Long Binary and Memo **Field** objects, **Size** is always set to 0. Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="c7e09-131">例</span><span class="sxs-lookup"><span data-stu-id="c7e09-131">Example</span></span>

<span data-ttu-id="c7e09-132">次の例では、"Employees" テーブルの **Field** オブジェクトの名前とサイズを列挙することで、 **Size** プロパティの機能を示します。</span><span class="sxs-lookup"><span data-stu-id="c7e09-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
