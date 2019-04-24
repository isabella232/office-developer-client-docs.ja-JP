---
title: Field2 プロパティ (DAO)
TOCTitle: FieldSize Property
ms:assetid: d609801d-7761-663f-2840-de5923bb120c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835039(v=office.15)
ms:contentKeyID: 48547976
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052870
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a7dfeb33568664a6a75f9f43de64e0c24abeb09a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292805"
---
# <a name="field2fieldsize-property-dao"></a><span data-ttu-id="21428-102">Field2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="21428-102">Field2.FieldSize property (DAO)</span></span>


<span data-ttu-id="21428-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="21428-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="21428-104">メモリではなくデータベースで使用される、 [**Recordset**](fields-collection-dao.md) オブジェクトの [**Fields**](recordset-object-dao.md) コレクションに含まれるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の **Field2** オブジェクトのバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="21428-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **Field2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="21428-105">構文</span><span class="sxs-lookup"><span data-stu-id="21428-105">Syntax</span></span>

<span data-ttu-id="21428-106">*式*。"</span><span class="sxs-lookup"><span data-stu-id="21428-106">*expression* .FieldSize</span></span>

<span data-ttu-id="21428-107">\*式\***Field2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="21428-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21428-108">注釈</span><span class="sxs-lookup"><span data-stu-id="21428-108">Remarks</span></span>

<span data-ttu-id="21428-109">[**AppendChunk**](field-appendchunk-method-dao.md) メソッドおよび [**GetChunk**](field-getchunk-method-dao.md) メソッドは、 **FieldSize** プロパティを指定すると、大きなフィールドを操作できます。</span><span class="sxs-lookup"><span data-stu-id="21428-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="21428-110">ロング バイナリ型 (Long Binary) またはメモ型 (Memo) のフィールドのサイズは 64K を超える可能性があるため、 **FieldSize** によって返された値は、長整数型 ( **Long**) の変数を格納できる大きさの変数に代入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21428-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="21428-111">メモ型 (Memo) およびロング バイナリ型 (Long Binary) 以外の **Field2** オブジェクトのサイズを確認するには、 **[Size](field-size-property-dao.md)** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="21428-111">To determine the size of a **Field2** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="21428-112">データベース サーバーまたは ODBC ドライバーがサーバー側カーソルをサポートしていない場合。</span><span class="sxs-lookup"><span data-stu-id="21428-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="21428-113">ODBC カーソル ライブラリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseODBC** に設定されているか、またはサーバーがサーバー側カーソルをサポートしていない状況で **dbUseDefault** に設定されている) 場合。</span><span class="sxs-lookup"><span data-stu-id="21428-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="21428-114">カーソルレス クエリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseNoCursor** に設定されている) 場合。</span><span class="sxs-lookup"><span data-stu-id="21428-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="21428-p101">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string. Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format. As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters. For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span><span class="sxs-lookup"><span data-stu-id="21428-p101">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string. Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format. As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters. For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="21428-119">例</span><span class="sxs-lookup"><span data-stu-id="21428-119">Example</span></span>

<span data-ttu-id="21428-120">次の使用例は、 **FieldSize** プロパティを使用して、2 つの異なるテーブルのメモ型 (Memo) とロング バイナリ型 (Long Binary) の Field オブジェクトで使用されるバイト数を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="21428-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="21428-p102">次の使用例では、 **AppendChunk** メソッドと **GetChunk** メソッドを使用して、別のレコードからのデータを一度に 32K ずつ読み込んで OLE オブジェクトのフィールドに設定します。実際のアプリケーションでは、たとえば、社員レコード (社員の写真を含む) をあるテーブルから別のテーブルにコピーするときに、このようなプロシージャを使用します。この使用例では、単にレコードを同じテーブルにコピーしています。すべてのブロック操作は、1 つの AddNew-Update シーケンス内で行われています。</span><span class="sxs-lookup"><span data-stu-id="21428-p102">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
